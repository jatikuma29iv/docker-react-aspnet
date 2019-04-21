# docker-react-aspnet
Full stack app with docker react and aspnet

# Run

## Install dependencies

```bash
docker-compose -f docker-compose.builder.yml run --rm install
```

## Run

```bash
docker-composer up
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


