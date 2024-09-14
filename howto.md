To build and launch a Docker image using the information in the Dockerfile, follow these steps:

1. Open a terminal or command prompt.
2. Navigate to the directory where the Dockerfile is located.
3. Run the following command to build the Docker image:
    ```
    docker build -t <image-name> .
    ```
    Replace `<image-name>` with the desired name for your Docker image.

4. Wait for the build process to complete. Docker will download any necessary dependencies and execute the instructions specified in the Dockerfile.

5. Once the build is finished, you can launch the Docker image using the following command:
    ```
    docker run -d -p <host-port>:<container-port> <image-name>
    ```
    Replace `<host-port>` with the port number on your host machine that you want to map to the container's port. Replace `<container-port>` with the port number specified in the Dockerfile or the one exposed by your application. Finally, replace `<image-name>` with the name of the Docker image you built.

6. Docker will start the container in detached mode (`-d` flag), allowing it to run in the background. You can now access your application by navigating to `http://localhost:<host-port>` in your web browser.

Remember to replace `<image-name>`, `<host-port>`, and `<container-port>` with your specific values.

## Exemple
`docker build -t roadmap-sh-local .`

`docker run -p 3000:3000 roadmap-sh-local`

All you have to do is to go to the your favorite navigator and enter : http://localhost:3000/