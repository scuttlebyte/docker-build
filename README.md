![](https://withsocial.com/assets/img/logo/withsocial.black.black.72ppi.png)

# WithSocial Laravel CI Builds

Run CI builds on your php/laravel applications with this repo which includes everything you need for standard/advanced Laravel tests. PHP 7.0-latest, Git, Composer, SQLite and any packages you need.

### Example usage with GitLab's `.gitlab-ci.yml`
```yml
# PHP 7.0
test:php7.0:
  image: bashy/docker-build:php70
  script:
  - vendor/bin/parallel-lint --exclude vendor --exclude _ide_helper.php .
  - vendor/bin/phpunit
  - vendor/bin/phpmd app/ text phpmd.xml
  - vendor/bin/phpcs --standard=psr2 app
```

## See master branch for full README!
