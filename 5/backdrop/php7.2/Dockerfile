### THIS FILE GENERATED BY https://github.com/michaelmcandrew/civicrm-docker/blob/master/generate.py ###

FROM php:7.2-apache

# libc-client-dev and libkrb5-dev required for the imap php extension
# libicu-dev required for the intl php extension
# libmagickwand-dev required for the imagick php extension
# libjpeg62-turbo-dev and libpng-dev required for the gd php extension
# libxml2-dev required for the soap php extension
# iproute2 is required to get the host ip at runtime for XDEBUG_REMOTE_HOST environment variable
# msmtp-mta allows us to globally redirect email via SMTP
# unzip is required for composer

RUN apt-get update \
  && apt-get install -y --no-install-recommends \
  iproute2 \
  less \
  libc-client-dev \
  libicu-dev \
  libjpeg62-turbo-dev \
  libkrb5-dev \
  libmagickwand-dev \
  libpng-dev \
  libxml2-dev \
  libzip-dev \
  msmtp-mta \
  mysql-client \
  unzip \
  wget \
  && rm -r /var/lib/apt/lists/*

# CiviCRM requires the following PHP extensions (some of which are already
# enabled in the Docker image:
#
# * curl (already enabled)
# * gd
# * gettext
# * imap
# * intl
# * json (already enabled)
# * mbstring (already enabled)
# * mysqli
# * openssl (already enabled)
# * pdo_mysql
# * phar (already enabled)
# * posix (already enabled)
# * soap
# * zip

# Configure and install php extensions (not configuration comes before installation)

RUN docker-php-ext-install bcmath \
  && docker-php-ext-configure gd --with-jpeg-dir=/usr/include/ --with-png-dir=/usr/include/ \
  && docker-php-ext-install gd \
  && docker-php-ext-install gettext \
  && docker-php-ext-configure imap --with-kerberos --with-imap-ssl \
  && docker-php-ext-install imap \
  && docker-php-ext-install intl \
  && docker-php-ext-install mysqli \
  && docker-php-ext-install opcache \
  && docker-php-ext-install pdo_mysql \
  && docker-php-ext-install soap \
  && docker-php-ext-install zip

# Install and enable imagick PECL extensions

RUN pecl install imagick \
  && docker-php-ext-enable imagick

# Install xdebug PECL extension
RUN pecl install xdebug

# Install composer using the method described at https://getcomposer.org/download/ (TODO consider whether this is really necessary - we could remove from this image)
RUN EXPECTED_SIGNATURE="$(curl https://composer.github.io/installer.sig)" \
  && php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
  && ACTUAL_SIGNATURE="$(php -r "echo hash_file('sha384', 'composer-setup.php');")" \
  && if [ "$EXPECTED_SIGNATURE" != "${ACTUAL_SIGNATURE}" ]; then >&2 echo 'ERROR: Invalid installer signature'; rm composer-setup.php; exit 1; fi \
  && php composer-setup.php --install-dir=/usr/local/bin --filename=composer \
  && rm composer-setup.php

# Create civicrm user

RUN useradd civicrm --home-dir /home/civicrm --create-home 

RUN chown -R civicrm:civicrm /var/www 

ENV APACHE_RUN_USER=civicrm

USER civicrm

RUN composer global require consolidation/cgr

USER root

# Download cv

RUN curl -LsS https://download.civicrm.org/cv/cv.phar -o /usr/local/bin/cv \
  && chmod +x /usr/local/bin/cv

# Download civix

RUN curl -LsS https://download.civicrm.org/civix/civix.phar -o /usr/local/bin/civix \
  && chmod +x /usr/local/bin/civix

# Configure apache

RUN a2enmod rewrite headers

COPY ./apache.conf /etc/apache2/conf-available/civicrm.conf

RUN a2enconf civicrm

# Configure php

RUN cp /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini

COPY ./civicrm-docker-load /usr/local/bin

COPY ./civicrm_dump.php /usr/local/src/civicrm_dump.php

RUN mkdir /usr/local/etc/civicrm

ENTRYPOINT [ "civicrm-docker-entrypoint" ]

CMD ["apache2-foreground"]

ENV CIVICRM_UF=Backdrop

USER civicrm

ENV PATH="/home/civicrm/.composer/vendor/bin:${PATH}"

RUN cgr drush/drush:~8

RUN mkdir -p /home/civicrm/.drush/commands \
    && cd /home/civicrm/.drush/commands \
    && curl -L https://github.com/backdrop-contrib/drush/releases/download/0.1.0/drush.zip > drush.zip \
    && unzip drush.zip -d backdrop \
    && rm drush.zip

RUN cd /var/www \
    && rmdir html \
    && drush dlb backdrop --path="html"

RUN cd /var/www/html/modules \
    && curl -L https://download.civicrm.org/civicrm-5.13.4-backdrop.tar.gz > civicrm-backdrop.tar.gz \
    && tar xzf civicrm-backdrop.tar.gz \
    && rm civicrm-backdrop.tar.gz

RUN cd /var/www/html/modules \
    && curl -L https://download.civicrm.org/civicrm-5.13.4-l10n.tar.gz > civicrm-l10n.tar.gz \
    && tar xzf civicrm-l10n.tar.gz \
    && rm civicrm-l10n.tar.gz

USER root

COPY ./civicrm-docker-entrypoint ./civicrm-docker-init ./civicrm-docker-dump ./civicrm-docker-install /usr/local/bin/

RUN mkdir -p /var/www/config/active \
    && mkdir -p /var/www/config/staging \
    && chown civicrm:civicrm /var/www/config/*

COPY --chown=civicrm:civicrm ./settings.php /usr/local/etc/civicrm

COPY --chown=civicrm:civicrm ./civicrm.settings.php /usr/local/etc/civicrm
