# CiviCRM on docker

An opinionated repository for production hosting of CiviCRM on Docker (your opinions on how it could be improved are very welcome).

All images are based php-apache.

In most cases, just choose the CMS that you would like to use, e.g. `civicrm:wordpress`. Everything else (php version, etc.) will be set to sensible defaults. You can get more specific with one of the tags below.

## Health warning

**WORK IN PROGRESS - USE AT YOUR OWN RISK**.

These images are largely untested in production.  Questions about how to use these images are very welcome in the issue queue. Answers will likely come in the form of updates to this README.md and other bits of documentation. Please share your experiences using these images so we can improve them as we go.

Implementation may well be behind the documentation for some CMS. If you are having difficulty getting going, please ping michaelmcandrew in the CiviCRM docker chat channel here:  https://chat.civicrm.org/civicrm/channels/docker and I will try and help, else feel free to create and issue.

## Tags

The following tags are available:

<!---START_TAGS-->
* `5.17.4-drupal-php7.3-variantapache` `5.17-drupal-php7.3-variantapache` `5-drupal-php7.3-variantapache` `5.17.4-drupal-php7.3` `5.17-drupal-php7.3` `5-drupal-php7.3` `5.17.4-php7.3-variantapache` `5.17-php7.3-variantapache` `5-php7.3-variantapache` `5.17.4-php7.3` `5.17-php7.3` `5-php7.3` `drupal-php7.3-variantapache` `drupal-php7.3` `php7.3-variantapache` `php7.3` [(5/drupal/php7.3/apache)](5/drupal/php7.3/apache)
* `5.17.4-drupal-php7.3-variantfpm` `5.17-drupal-php7.3-variantfpm` `5-drupal-php7.3-variantfpm` `5.17.4-php7.3-variantfpm` `5.17-php7.3-variantfpm` `5-php7.3-variantfpm` `drupal-php7.3-variantfpm` `php7.3-variantfpm` [(5/drupal/php7.3/fpm)](5/drupal/php7.3/fpm)
* `5.17.4-drupal-php7.2-variantapache` `5.17-drupal-php7.2-variantapache` `5-drupal-php7.2-variantapache` `5.17.4-drupal-php7.2` `5.17-drupal-php7.2` `5-drupal-php7.2` `5.17.4-drupal-variantapache` `5.17-drupal-variantapache` `5-drupal-variantapache` `5.17.4-drupal` `5.17-drupal` `5-drupal` `5.17.4-php7.2-variantapache` `5.17-php7.2-variantapache` `5-php7.2-variantapache` `5.17.4-php7.2` `5.17-php7.2` `5-php7.2` `5.17.4-variantapache` `5.17-variantapache` `5-variantapache` `5.17.4` `5.17` `5` `drupal-php7.2-variantapache` `drupal-php7.2` `drupal-variantapache` `drupal` `php7.2-variantapache` `php7.2` `variantapache` `latest` [(5/drupal/php7.2/apache)](5/drupal/php7.2/apache)
* `5.17.4-drupal-php7.2-variantfpm` `5.17-drupal-php7.2-variantfpm` `5-drupal-php7.2-variantfpm` `5.17.4-drupal-variantfpm` `5.17-drupal-variantfpm` `5-drupal-variantfpm` `5.17.4-php7.2-variantfpm` `5.17-php7.2-variantfpm` `5-php7.2-variantfpm` `5.17.4-variantfpm` `5.17-variantfpm` `5-variantfpm` `drupal-php7.2-variantfpm` `drupal-variantfpm` `php7.2-variantfpm` `variantfpm` [(5/drupal/php7.2/fpm)](5/drupal/php7.2/fpm)
* `5.17.4-drupal-php7.1-variantapache` `5.17-drupal-php7.1-variantapache` `5-drupal-php7.1-variantapache` `5.17.4-drupal-php7.1` `5.17-drupal-php7.1` `5-drupal-php7.1` `5.17.4-php7.1-variantapache` `5.17-php7.1-variantapache` `5-php7.1-variantapache` `5.17.4-php7.1` `5.17-php7.1` `5-php7.1` `drupal-php7.1-variantapache` `drupal-php7.1` `php7.1-variantapache` `php7.1` [(5/drupal/php7.1/apache)](5/drupal/php7.1/apache)
* `5.17.4-drupal-php7.1-variantfpm` `5.17-drupal-php7.1-variantfpm` `5-drupal-php7.1-variantfpm` `5.17.4-php7.1-variantfpm` `5.17-php7.1-variantfpm` `5-php7.1-variantfpm` `drupal-php7.1-variantfpm` `php7.1-variantfpm` [(5/drupal/php7.1/fpm)](5/drupal/php7.1/fpm)
* `5.17.4-drupal-php7.0-variantapache` `5.17-drupal-php7.0-variantapache` `5-drupal-php7.0-variantapache` `5.17.4-drupal-php7.0` `5.17-drupal-php7.0` `5-drupal-php7.0` `5.17.4-php7.0-variantapache` `5.17-php7.0-variantapache` `5-php7.0-variantapache` `5.17.4-php7.0` `5.17-php7.0` `5-php7.0` `drupal-php7.0-variantapache` `drupal-php7.0` `php7.0-variantapache` `php7.0` [(5/drupal/php7.0/apache)](5/drupal/php7.0/apache)
* `5.17.4-drupal-php7.0-variantfpm` `5.17-drupal-php7.0-variantfpm` `5-drupal-php7.0-variantfpm` `5.17.4-php7.0-variantfpm` `5.17-php7.0-variantfpm` `5-php7.0-variantfpm` `drupal-php7.0-variantfpm` `php7.0-variantfpm` [(5/drupal/php7.0/fpm)](5/drupal/php7.0/fpm)
* `5.17.4-drupal-php5.6-variantapache` `5.17-drupal-php5.6-variantapache` `5-drupal-php5.6-variantapache` `5.17.4-drupal-php5.6` `5.17-drupal-php5.6` `5-drupal-php5.6` `5.17.4-php5.6-variantapache` `5.17-php5.6-variantapache` `5-php5.6-variantapache` `5.17.4-php5.6` `5.17-php5.6` `5-php5.6` `drupal-php5.6-variantapache` `drupal-php5.6` `php5.6-variantapache` `php5.6` [(5/drupal/php5.6/apache)](5/drupal/php5.6/apache)
* `5.17.4-drupal-php5.6-variantfpm` `5.17-drupal-php5.6-variantfpm` `5-drupal-php5.6-variantfpm` `5.17.4-php5.6-variantfpm` `5.17-php5.6-variantfpm` `5-php5.6-variantfpm` `drupal-php5.6-variantfpm` `php5.6-variantfpm` [(5/drupal/php5.6/fpm)](5/drupal/php5.6/fpm)
* `5.17.4-wordpress-php7.3-variantapache` `5.17-wordpress-php7.3-variantapache` `5-wordpress-php7.3-variantapache` `5.17.4-wordpress-php7.3` `5.17-wordpress-php7.3` `5-wordpress-php7.3` `wordpress-php7.3-variantapache` `wordpress-php7.3` [(5/wordpress/php7.3/apache)](5/wordpress/php7.3/apache)
* `5.17.4-wordpress-php7.3-variantfpm` `5.17-wordpress-php7.3-variantfpm` `5-wordpress-php7.3-variantfpm` `wordpress-php7.3-variantfpm` [(5/wordpress/php7.3/fpm)](5/wordpress/php7.3/fpm)
* `5.17.4-wordpress-php7.2-variantapache` `5.17-wordpress-php7.2-variantapache` `5-wordpress-php7.2-variantapache` `5.17.4-wordpress-php7.2` `5.17-wordpress-php7.2` `5-wordpress-php7.2` `5.17.4-wordpress-variantapache` `5.17-wordpress-variantapache` `5-wordpress-variantapache` `5.17.4-wordpress` `5.17-wordpress` `5-wordpress` `wordpress-php7.2-variantapache` `wordpress-php7.2` `wordpress-variantapache` `wordpress` [(5/wordpress/php7.2/apache)](5/wordpress/php7.2/apache)
* `5.17.4-wordpress-php7.2-variantfpm` `5.17-wordpress-php7.2-variantfpm` `5-wordpress-php7.2-variantfpm` `5.17.4-wordpress-variantfpm` `5.17-wordpress-variantfpm` `5-wordpress-variantfpm` `wordpress-php7.2-variantfpm` `wordpress-variantfpm` [(5/wordpress/php7.2/fpm)](5/wordpress/php7.2/fpm)
* `5.17.4-wordpress-php7.1-variantapache` `5.17-wordpress-php7.1-variantapache` `5-wordpress-php7.1-variantapache` `5.17.4-wordpress-php7.1` `5.17-wordpress-php7.1` `5-wordpress-php7.1` `wordpress-php7.1-variantapache` `wordpress-php7.1` [(5/wordpress/php7.1/apache)](5/wordpress/php7.1/apache)
* `5.17.4-wordpress-php7.1-variantfpm` `5.17-wordpress-php7.1-variantfpm` `5-wordpress-php7.1-variantfpm` `wordpress-php7.1-variantfpm` [(5/wordpress/php7.1/fpm)](5/wordpress/php7.1/fpm)
* `5.17.4-wordpress-php7.0-variantapache` `5.17-wordpress-php7.0-variantapache` `5-wordpress-php7.0-variantapache` `5.17.4-wordpress-php7.0` `5.17-wordpress-php7.0` `5-wordpress-php7.0` `wordpress-php7.0-variantapache` `wordpress-php7.0` [(5/wordpress/php7.0/apache)](5/wordpress/php7.0/apache)
* `5.17.4-wordpress-php7.0-variantfpm` `5.17-wordpress-php7.0-variantfpm` `5-wordpress-php7.0-variantfpm` `wordpress-php7.0-variantfpm` [(5/wordpress/php7.0/fpm)](5/wordpress/php7.0/fpm)
* `5.17.4-wordpress-php5.6-variantapache` `5.17-wordpress-php5.6-variantapache` `5-wordpress-php5.6-variantapache` `5.17.4-wordpress-php5.6` `5.17-wordpress-php5.6` `5-wordpress-php5.6` `wordpress-php5.6-variantapache` `wordpress-php5.6` [(5/wordpress/php5.6/apache)](5/wordpress/php5.6/apache)
* `5.17.4-wordpress-php5.6-variantfpm` `5.17-wordpress-php5.6-variantfpm` `5-wordpress-php5.6-variantfpm` `wordpress-php5.6-variantfpm` [(5/wordpress/php5.6/fpm)](5/wordpress/php5.6/fpm)
* `5.17.4-backdrop-php7.3-variantapache` `5.17-backdrop-php7.3-variantapache` `5-backdrop-php7.3-variantapache` `5.17.4-backdrop-php7.3` `5.17-backdrop-php7.3` `5-backdrop-php7.3` `backdrop-php7.3-variantapache` `backdrop-php7.3` [(5/backdrop/php7.3/apache)](5/backdrop/php7.3/apache)
* `5.17.4-backdrop-php7.3-variantfpm` `5.17-backdrop-php7.3-variantfpm` `5-backdrop-php7.3-variantfpm` `backdrop-php7.3-variantfpm` [(5/backdrop/php7.3/fpm)](5/backdrop/php7.3/fpm)
* `5.17.4-backdrop-php7.2-variantapache` `5.17-backdrop-php7.2-variantapache` `5-backdrop-php7.2-variantapache` `5.17.4-backdrop-php7.2` `5.17-backdrop-php7.2` `5-backdrop-php7.2` `5.17.4-backdrop-variantapache` `5.17-backdrop-variantapache` `5-backdrop-variantapache` `5.17.4-backdrop` `5.17-backdrop` `5-backdrop` `backdrop-php7.2-variantapache` `backdrop-php7.2` `backdrop-variantapache` `backdrop` [(5/backdrop/php7.2/apache)](5/backdrop/php7.2/apache)
* `5.17.4-backdrop-php7.2-variantfpm` `5.17-backdrop-php7.2-variantfpm` `5-backdrop-php7.2-variantfpm` `5.17.4-backdrop-variantfpm` `5.17-backdrop-variantfpm` `5-backdrop-variantfpm` `backdrop-php7.2-variantfpm` `backdrop-variantfpm` [(5/backdrop/php7.2/fpm)](5/backdrop/php7.2/fpm)
* `5.17.4-backdrop-php7.1-variantapache` `5.17-backdrop-php7.1-variantapache` `5-backdrop-php7.1-variantapache` `5.17.4-backdrop-php7.1` `5.17-backdrop-php7.1` `5-backdrop-php7.1` `backdrop-php7.1-variantapache` `backdrop-php7.1` [(5/backdrop/php7.1/apache)](5/backdrop/php7.1/apache)
* `5.17.4-backdrop-php7.1-variantfpm` `5.17-backdrop-php7.1-variantfpm` `5-backdrop-php7.1-variantfpm` `backdrop-php7.1-variantfpm` [(5/backdrop/php7.1/fpm)](5/backdrop/php7.1/fpm)
* `5.17.4-backdrop-php7.0-variantapache` `5.17-backdrop-php7.0-variantapache` `5-backdrop-php7.0-variantapache` `5.17.4-backdrop-php7.0` `5.17-backdrop-php7.0` `5-backdrop-php7.0` `backdrop-php7.0-variantapache` `backdrop-php7.0` [(5/backdrop/php7.0/apache)](5/backdrop/php7.0/apache)
* `5.17.4-backdrop-php7.0-variantfpm` `5.17-backdrop-php7.0-variantfpm` `5-backdrop-php7.0-variantfpm` `backdrop-php7.0-variantfpm` [(5/backdrop/php7.0/fpm)](5/backdrop/php7.0/fpm)
* `5.17.4-backdrop-php5.6-variantapache` `5.17-backdrop-php5.6-variantapache` `5-backdrop-php5.6-variantapache` `5.17.4-backdrop-php5.6` `5.17-backdrop-php5.6` `5-backdrop-php5.6` `backdrop-php5.6-variantapache` `backdrop-php5.6` [(5/backdrop/php5.6/apache)](5/backdrop/php5.6/apache)
* `5.17.4-backdrop-php5.6-variantfpm` `5.17-backdrop-php5.6-variantfpm` `5-backdrop-php5.6-variantfpm` `backdrop-php5.6-variantfpm` [(5/backdrop/php5.6/fpm)](5/backdrop/php5.6/fpm)
<!---END_TAGS-->

## 'Quick' start

There are a couple of options for getting started. Here are a couple of common workflows that I use.

If I plan on doing a fair amount of custom development as part of a project, I like to start with a 'mono repo' on the host machine containing everything from the CMS root downwards (excluding files with credentials in and folders that include uploads via the webserver). This makes working with IDEs, debugging, etc. more simple.

If you aren't planning on doing much custom development (e.g. maybe you are just installing already existing modules and extensions) it might make more sense to take advantage of the CMS  and CiviCRM already installed on the image (at `/var/www/html`).

To get a local project up and running, choose your CMS flavour  from the [docker-compose](docker-compose) and copy the entire directory to somewhere like `~/projects/backdrop-example-project`

1. Copy the `dev.dist.env` file to `.env`. and edit as appropriate (choose sensible passwords, set the base url and other required environment variables, e.g. the domain you want the site to be available at.
2. Copy `docker-compose.dev.dist.yml` to `docker-compose.yml` and assign port numbers as appropriate (see *Reverse proxies* for more details).
3. *If you are mounting a mono repo from the host to the container* (see above), place it in  the `src` folder, and uncomment the `./src:/var/www/html` volume.
4. *If you want development site to be available at a memorable address and/or you want to serve it via https*, configure it now.
5. Run `docker-compose up -d`
6. Install a new site with something like `docker-compose exec civicrm civicrm-docker-install` .

Note that if you already have a dump containing the database and file dump (in the format expected by civicrm-docker) you do not need to install the CMS and CiviCRM. You can just initialise it with  `docker-compose exec civicrm civicrm-docker-install`  and then follow the load instructions below.

## Dumping state

Running `docker-compose exec civicrm civicrm-docker-dump`  will place a database and file dump in the `/state` folder of the container (which is mapped to the `./state` sub-folder in your docker-compose root on the host).

## Loading state

 Running `docker-compose exec civicrm civicrm-docker-load`  will load an existing database dump from the `/state` folder of the container (which is mapped to the `./state` sub-folder in your docker-compose root on the host.

# Reverse proxy

You may wish to reverse proxy your site so that it is available at a nice looking domain like https://example.com, rather than, e.g.  http://localhost:8888. Here is a suitable snippet for nginx to get you started

```
server {
    listen 80;
    server_name example.com;
    return 301 https://$host$request_uri;
}
server {
    listen 443 ssl;
    server_name example.com;

    include snippets/snakeoil.conf;

    location / {
        proxy_pass http://localhost:8888;
        proxy_set_header Host $host;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header X-Real-IP $remote_addr;
	    proxy_read_timeout 300s;
	    proxy_send_timeout 300s;
    }
}
```
# MySQL

The images are designed to be used with whatever MySQL backend you like: one in a container, one on bare metal, or maybe a DB appliance from a cloud provider.

A simple mysql image based on  the official `mysql:5.6` and suitable for CiviCRM can be found at `michaelmcandrew/mysql-civicrm`. See the `docker-compose.dev.dist.yml` files in the docker-compose directory for an example of this image in use.

## Source code

For convenience, a zip of the original source code of CiviCRM and the selected CMS can* be found at `/usr/local/src`.

  *Not quite ready yet!

## Administration

Steps up update this repository.

`generate.py` automates the generation of Dockerfiles (updates combos.json).
`build.py` builds images based on the dockerfiles (based on combos.json).
`publish.py` publishes these images on dockerhub (based on combos.json).

Note, at the moment, this is a manual process. It would be good to automate this, either nightly, or whenever a new release of CiviCRM or any of the CMSes, or an update of the base php image they are derived from comes out.

## Adding contributed code

There are .txt files in the `templates` folder that are used to download code for contributed modules/plugins, layouts, and civicrm extensions.

Extensions listed in civicrm_extension_download.txt are downloaded with the `cv` utility and should be formatted as such:

```
sample@https://lab.civicrm.org/sample/civicrm-advanced-events/-/archive/master/sampleextension-master.zip
--dev shoreditch

```

Backdrop and Drupal modules are downloaded with `drush dl`

```
passphrase_policy --dev
better_exposed_filters

```
