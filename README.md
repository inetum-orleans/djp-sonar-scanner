# djp-template

A [ddb](https://inetum-orleans.github.io/docker-devbox-ddb) jsonnet package (**djp**).

## Description

[Sonar Scanner](https://docs.sonarqube.org/latest/analysis/scan/sonarscanner/) **djp** package.

## Snippet

- `ddb.yml`

```yaml
cookiecutter:
  templates:
    - template: gh:inetum-orleans/djp-sonar-scanner
```

- `docker-compose.yml.jsonnet`

```jsonnet
ddb.Compose(
  ddb.with(
    import '.docker/sonar-scanner/djp.libjsonnet',
    params={global: true}
  )
)
```

## Parameters

| name  | type | description |
| ------------- | ------------- | ------------- |
| global  | boolean  | Should the binary be global ?

## Usage

Please check [jsonnet feature](https://inetum-orleans.github.io/docker-devbox-ddb/features/jsonnet/#ddb-jsonnet-packages-djp)
to understand how to include a **djp** package inside a [ddb](https://inetum-orleans.github.io/docker-devbox-ddb) project.

Looking for other [djp packages](https://github.com/inetum-orleans?q=djp-) ? Check github repositories starting with `djp-`.
