# Docker Interview Questions & Answers

#### 1. Docker container will get reboot failure what you will do if it won't work ?
**Answer.** If a Docker container faces reboot failure, I would first investigate the container logs using the docker logs command to identify any error messages or issues. I might also check the container's configuration and dependencies. If the problem persists, I may try restarting the Docker daemon, updating Docker, or recreating the container with proper configurations. If all else fails, I may need to troubleshoot the underlying host system or consult Docker community forums for assistance.

#### 2. Write a docker file to copy a file from the system to container with a volume mount?
**Answer.**
```
FROM ubuntu:latest
# Create a directory in the container
WORKDIR /app
# Copy a file from the host system to the container
COPY ./localfile.txt /app/
# Define a volume mount
VOLUME /app/data
# Set the working directory
WORKDIR /app/data
```

#### 3. What is docker networks?
**Answer.** Docker Networks are vital for defining communication patterns, ensuring proper isolation, and facilitating containerized application deployment.
