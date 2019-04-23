# docker-react-aspnet
Full stack app with docker react and aspnet

# Checkout & Run

## Checkout

```bash
git clone git@github.com:jatikuma29iv/docker-react-aspnet.git
cd docker-react-aspnet
git submodule update --init --recursive
```

## Install dependencies

```bash
docker-compose -f docker-compose.builder.yml run --rm install
docker-compose build
```

## Run

```bash
docker-composer up
```

## Server startup failed

If any `resource` fails to start, enable them one by one

```bash
# start Oracle DB
docker-compose up oracledb

# start keycloak
docker-compose up keycloak

# start Elasticsearch
docker-compose up es01
```

# Setup

## React

### Install React

```bash
npm install -g create-react-app
```

### Create New App

```bash
create-react-app app-core
```

### Build & Run with Docker

```
cd app-core

# copies src to image & run commands of build section
docker build -t "app-core:Dockerfile" .

# run the app
docker run -it -p 3000:3000 "app-core:Dockerfile"
```

### Build & Run

```bash
cd app-core

npm install
npm start
```


