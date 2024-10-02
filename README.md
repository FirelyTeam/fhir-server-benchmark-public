# fhir-server-benchmark-public
Settings used for benchmarking FHIR server

In order to start the docker-compose, you need first to create a file `.env` with a content similar to:
```INI
# SqlServer
SQLDB_PASSWORD="SomeStringPassword"

```

Once this is done, you can start using:

```SH
sudo docker compose up
```
