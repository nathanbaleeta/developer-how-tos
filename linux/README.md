# Linux commands

#### Setup [Apache Nifi](https://nifi.apache.org/) using Docker
Once docker setup completes, access browser via https://localhost:8443/nifi
```
docker run --name nifi \
  -p 8443:8443 \
  -d \
  apa
