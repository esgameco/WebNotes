# Basic Docker

## Creating and Running a Docker Image

Step 1: Clone repository

```bash
docker run --name repo alpine/git clone {url}
```

Step 2: Build docker image

```bash
docker build -t {imageName} .
```

Step 3: Run docker image

```bash
docker run -d -p 80:80 --name {instanceName} {imageName}
```