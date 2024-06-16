# Docker Protoc Generator for go-micro

This is a docker image for [go-micro/generator](https://github.com/go-micro/generator)

### Repository Structure

```
|-- Dockerfile                  # The main Dockerfile for the image
|-- docker_entrypoint.sh        # The main script for generating the go files
|-- Makefile                    # The project Makefile
```

### Building the Image

To build the docker image, run the following command:

```
make    # or `make build`
```

### Using the image

To generate the go files, run the following command:

```
docker run -it --rm \
    -v $(pwd)/proto:/proto \
    -v $(pwd)/build:/build \
    protoc-go-micro:latest /proto /build
```