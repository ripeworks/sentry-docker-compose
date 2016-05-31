```
# Set POSTGRES_DB_PASSWORD in docker-compose.yml
$ docker-compose up -d redis
$ docker-compose up -d postgres
$ docker-compose run --rm sentry generate-secret-key
# Add output to SENTRY_SECRET_KEY in docker-compose.yml
$ docker-compose run --rm sentry upgrade
$ docker-compose run sentry celery beat
$ docker-compose run sentry celery worker
```
