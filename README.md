# CORS Proxy for Heritage Connector

Allows [Thor SPARQL client](https://github.com/TheScienceMuseum/thor-docker
) to work with [Docker hosted Fuseki](https://github.com/TheScienceMuseum/fuseki-docker)

## Requirements 

- [Docker hosted Fuseki](https://github.com/TheScienceMuseum/fuseki-docker) running on port 3030
- [Thor SPARQL client](https://github.com/TheScienceMuseum/thor-docker running on port 80

Enter host:8080 as your SPARQL endpoint in Thir (which will now proxied from Fuseki with the correct CORS headers)

## Usage (local)

### To build:

``` bash
docker build --no-cache . -t thor-cors-proxy
```

### To run:

``` bash
docker run -p 8080:8080 thor-cors-proxy
```

We use the `-d` and `--restart=always` flags to make it automatically restart.

Help (all run options explained):

``` bash
docker run --rm fuseki --help
```
