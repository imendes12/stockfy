# Docker Compose Documentation

## Getting Started

This command starts and runs an entire application defined in a `compose.yaml` file. It orchestrates all services specified within the configuration, bringing up all necessary containers.

[Source](https://github.com/docker/compose/blob/main/README.md#_snippet_0)

```bash
docker compose up
```

This YAML configuration defines two services, 'web' and 'redis', for a multi-container application. The 'web' service builds from the current directory, exposes port 5000, and mounts the current directory as a volume. The 'redis' service leverages the official Redis Docker image.

[Source](https://github.com/docker/compose/blob/main/README.md#_snippet_1)

```yaml
services:
  web:
    build: .
    ports:
      - "5000:5000"
    volumes:
      - .:/code
  redis:
    image: redis
```

## Building

This command compiles the Docker Compose CLI plugin for the host machine. It requires 'make' and 'go' to be installed as prerequisites, as specified in the project's go.mod file. The resulting binary will be placed in the `./bin/build` directory.

[Source](https://github.com/docker/compose/blob/main/BUILDING.md#_snippet_0)

```console
make
```

## Running Tests

Execute all unit tests defined within the Docker Compose CLI project. This command uses the 'make' utility to invoke the project's test suite. To update golden files during testing, use the 'go test' command with the '-test.update-golden' flag.

[Source](https://github.com/docker/compose/blob/main/BUILDING.md#_snippet_1)

```console
make test
```

```console
go test ./... -test.update-golden
```
