# 8.6 caused an exit code 100, not sure why
# 9.5.10 caused a problem with postgres in docker-compose
# Both working now
FROM drupal:9.5.10

RUN apt-get update && apt-get install -y git \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /var/www/html/themes

RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupal.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap
