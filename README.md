[![tests](https://github.com/ddev/ddev-addon-template/actions/workflows/tests.yml/badge.svg)](https://github.com/ddev/ddev-addon-template/actions/workflows/tests.yml) ![project is maintained](https://img.shields.io/maintenance/yes/2024.svg)

# GraphQL ddev Add-on

## Getting started

In the DDEV project directory:

For DDEV v1.23.5 or above run

```sh
ddev add-on get machine-rc/graphql
```

For earlier versions of DDEV run

```sh
ddev get machine-rc/graphql
```

Restart the DDEV instance:

```sh
ddev restart
```

Open the Grafana web interface via the url: https://your-project-name.ddev.site:4000/

## Customizations
Current structure allows support for multiple graphql services. 
To add a new service:
- create a new directory in the `graphql` directory with the service name
- copy the `Dockerfile` from the `graphql/book` directory
- adjust `docker-compose.graphql.yaml` to include the new service by duplicating the `graphql-book` service and changing the service name
  - adjust the `environment` section to expose the new service on a different port
