# Integration Tests Example

This project showcases how Ardan Labs handles integration tests in regards
to databases. The patterns and techniques used to write integration tests
with a database can also be applied to other services.

This repository runs a simple list daemon (`listd`) that implements a REST API
for lists and items in relation to lists. The daemon uses a postgres database
to persist data.

For information regarding the `listd` API, see the `apiary.apib` located in
`./cmd/listd/deploy/`.

## Running

The only dependencies to run this program are:

- `docker`
- `docker-compose`

To run the program simply execute the following command:

```shell
make run
```

This will stop any containers defined by the compose file if already running
and then rebuild the containers using the compose file. The list daemon (`listd`)
will be available at `localhost:3000` and the postgres instance will be available
at `localhost:5432`.