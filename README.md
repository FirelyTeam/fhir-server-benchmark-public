# fhir-server-benchmark-public
Settings used for benchmarking FHIR server

In order to start the docker-compose, you need first to create a file `.env` with a content similar to:
```INI
# SqlServer
SQLDB_PASSWORD="SomeStringPassword"
```
You also need to add a license for Firely Server called `firelyserver-license.json` in the folder.

Once this is done, you can start using:

```SH
sudo docker compose up
```

Once the docker services are up and running, you can start the benchmark using the following command:
```SH
sudo docker exec fhir-server-benchmark-public-fhir-benchmark-1 benchmark.sh -threads=8 -server_url="http://firelyserver:4080"
```

You can retrieve the stats while this is running using the following command:
```SH
while true; do sudo docker stats --no-stream | tee --append stats.txt; sleep 1; done
```