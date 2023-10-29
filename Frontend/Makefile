# Makefile for React Project

# Define the name of your Docker image
IMAGE_NAME = my-react-app

# Define the Docker container name
CONTAINER_NAME = my-react-app-container

# Define the port for your development server
DEV_SERVER_PORT = 3000

# Default target: build and run the app
all: stop build run

# Build the Docker image
build:
	docker build -t $(IMAGE_NAME) .

# Run the Docker container
run:
	docker run -d -p $(DEV_SERVER_PORT):$(DEV_SERVER_PORT) --name $(CONTAINER_NAME) $(IMAGE_NAME)

# Stop and remove the Docker container
stop:
	docker stop $(CONTAINER_NAME) || true
	docker rm $(CONTAINER_NAME) || true

# Clean up the Docker image and remove the container
clean: stop
	docker rmi $(IMAGE_NAME)


CONTAINER_CMD = npm start

# Run the Docker container and execute a command inside it
exec:
	docker exec -it $(CONTAINER_NAME) $(CONTAINER_CMD)

.PHONY: all build run stop clean
