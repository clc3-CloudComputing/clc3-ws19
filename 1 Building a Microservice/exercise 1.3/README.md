# Exercise 1.3: Run a Docker container with a Microservice

In this exercise, you will build a Docker image from a Dockerfile and then run a container from this image.

## Instructions

1. Create image from the provided Dockerfile:

    ```console
    docker image build -t [your-dockerhub-account]/myhello:0.0.1 ./
    ```

1. Run the a container from the image and expose the container port: **8888** to the host port: **9090**.

    ```console
    docker container run -p 9090:8888 [your-dockerhub-account]/myhello:0.0.1
    ```

1. Open a browser and go to: https://localhost:9090

1. See your container running on your local Docker daemon:

    ```console
    docker ps
    ```
    
    ```
    CONTAINER ID        IMAGE                    COMMAND             CREATED             STATUS              PORTS                    NAMES
    789d08da1704        xyz/myhello:0.0.1        "/usr/myapp"        21 seconds ago      Up 19 seconds       0.0.0.0:9999->8888/tcp   foxy_joliot
    ```

1. Stop your container:

    ```console
    docker stop 789d08da1704
    ```
