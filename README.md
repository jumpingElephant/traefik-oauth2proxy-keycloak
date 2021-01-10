# traefik - OAuth2 Proxy - Keycloak

Test environment for securing web apps using [OAuth2 Proxy](https://github.com/oauth2-proxy/oauth2-proxy) and
[Keycloak](https://www.keycloak.org/) as identity provider, where all services live behind the reverse proxy
[traefik](https://traefik.io/traefik/).

The architecture can be inspected on the OAuth2 Proxy [website](https://oauth2-proxy.github.io/oauth2-proxy/).

## Preparation

OAuth2 Proxy is used in a development version of master branch, some time after v6.1.1, to take advantage of alpha config: commit 597ffeb1217058afd71182e8cec1de670f8b6998

The image used for testing can be build by running the following command after OAuth2-Proxy-repository was
cloned:

`
docker build --tag alex/oauth2-proxy:v6.1.2-alpha .
`

## Run test environment

Run it using the provided Docker Compose configuration:

`
docker-compose up
`

then the [HTML5 UP](http://html5up.net/) based site can be viewed in the browser using this link
to [localhost](http://localhost:80/).
If asked: credentials to sign in are admin:password