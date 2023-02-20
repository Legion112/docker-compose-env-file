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