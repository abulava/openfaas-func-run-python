# Run Python 2.7 code as a function

## Usage: deploy on [OpenFaaS](https://www.openfaas.com)

### Prerequisites for deploying remotely as an authenticated user

```
echo "<password>" | faas-cli login -g <gateway URL> -u <username> --password-stdin
```

### Workflow

```
faas-cli deploy -g <gateway URL> -f ./stack.yml
```

## Development: build and push to [Docker Hub](https://hub.docker.com/)

### Prerequisites

```
echo "<password>" | docker login -u abulava --password-stdin
```

### Workflow

```
faas-cli build -f ./stack.yml
faas-cli push -f ./stack.yml
```
