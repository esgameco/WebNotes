# Install Postgres

### Install locally

[https://www.postgresql.org/download/](https://www.postgresql.org/download/)

### Docker install

```bash
docker pull postgres
docker run --name {name} -e POSTGRES_PASSWORD={password} -d postgres
```

[Documentation](https://hub.docker.com/_/postgres)