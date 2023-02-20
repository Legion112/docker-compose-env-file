# RUN
```
VARIABLE_FROM_DOT_ENV_DOCKER=somevalue docker compose run --rm app
```

What should you not see is:
```
WARN[0000] The "VARIABLE_FROM_DOT_ENV" variable is not set. Defaulting to a blank string. 
WARN[0000] The "VARIABLE_FROM_DOT_ENV" variable is not set. Defaulting to a blank string. 
WARN[0000] The "VARIABLE_FROM_DOT_ENV" variable is not set. Defaulting to a blank string. 
```

Working way which remove all warning, but you have to pass `--env-file` to each cli call :-(
```
 VARIABLE_FROM_DOT_ENV_DOCKER=somevalue docker compose --env-file .env.docker run  --rm app
```

Feature which I request is to be able to set this value on `docker-compose` config level which reduce line length.