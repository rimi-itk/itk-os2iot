# ITK OS2OoT

## Development

``` shell name=start
task start
```

``` shell name=get-types
curl "http://$(task compose --silent -- port scorpio 9090)/ngsi-ld/v1/types"
```

## Production

Edit `.env.local` and set a proper domain and compose commands, e.g.

``` sh
# .env.local
COMPOSE_DOMAIN=itk-os2iot.srvitkstgweb02.itkdev.dk
TASK_DOCKER_COMPOSE='docker compose --env-file .env --env-file .env.local --file compose.yaml --file compose.prod.yaml'
```

``` shell name=prod-start
task start
```
