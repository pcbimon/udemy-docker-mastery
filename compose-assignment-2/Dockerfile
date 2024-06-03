# pull drupal:9
FROM drupal:9
#Then RUN apt package manager command to install git
RUN apt-get update \
    && apt-get install -y git \
    && rm -rf /var/lib/apt/lists/*
#Set the working directory to /var/www/html/themes
WORKDIR /var/www/html/themes
#Clone the bootstrap theme from drupalcode.org
RUN git clone --branch 8.x-4.x --single-branch --depth 1 https://git.drupalcode.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap
#Set the working directory to /var/www/html
WORKDIR /var/www/html