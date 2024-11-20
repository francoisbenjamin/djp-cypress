# djp-template

A [ddb](https://inetum-orleans.github.io/docker-devbox-ddb) jsonnet package (**djp**).

## Description

[Cypress](https://www.cypress.io/) djp package

## Snippet

- `ddb.yml`

```yaml
cookiecutter:
  templates:
    - template: gh:inetum-orleans/djp-cypress
      extra_context:
        cypress_version: 'browsers:node18.6.0-chrome105-ff104'
```

- `docker-compose.yml.jsonnet`

```jsonnet
ddb.Compose(
  ddb.with(
    import '.docker/cypress/djp.libjsonnet'
  )
)
```

## Parameters

| name            | type | description |
|-----------------| ------------- | ------------- |
| cypress_version | string  | The tag version of the Docker image of Cypress, ex : base:latest

## Usage

Please check [jsonnet feature](https://inetum-orleans.github.io/docker-devbox-ddb/features/jsonnet/#ddb-jsonnet-packages-djp)
to understand how to include a **djp** package inside a [ddb](https://inetum-orleans.github.io/docker-devbox-ddb) project.

Looking for other [djp packages](https://github.com/inetum-orleans?q=djp-) ? Check github repositories starting with `djp-`.
