# final_assignment_os
for challenge 3 and 4

## Introduction
This report documents the process and learnings from Docker Challenge 3. The primary objectives were to understand the interaction between different Docker components (services), utilize environment variables in the application's configuration, and orchestrate a multi-container setup with Docker Compose including a web server, application server, and a database.

## Procedure

### Environment Setup:
- Installed Docker Desktop on Windows.
- Prepared the project directory with the required Dockerfiles and configuration files for each service.

### Steps to Complete Challenge 3
1. Adjust the docker configuration files of api service and nginx service
2. Create .env file at the root of the directory to store the environment variables and define the variables for both the application server and the database.
3. Create docker-compose.yml file at the root of the directory to define api, database and nginx services and how they interact.
4. After creating both docker-compose.yml and .env files, build the services and test the services by using the below commands
    - `docker-compose up --build`  (to build the docker services)
    - `docker-compose ps`  (to check the docker services' status)
5. To verify if the services are running as expected, access the application by
    - http://localhost:8080/api/books
    - http://localhost:8080/api/books/1

### Steps to Complete Challenge 4
1. Accessing the application in the challenge 3 by
    - http://localhost:8080/api/stats
2. Access the application multiple times and record the "hostname"
3. To scale up the services to 3 instances by using the command
    - `docker-compose up -d --scale node-service=3`
4. To check if the services are running by using the command
    - `docker-compose ps` 
5. To ensure the new instances are working, refresh the services by using commands
    - `docker-compose restart` (to refresh the instances)
    - `docker-compose ps` (to check the status)
6. To verify if the application is running across the instances, access the application by
    - http://localhost:8080/api/stats
7. To see the differences between, access the application multiple times and record the "hostname"
8. When different hostnames are shown, challenge 4 is successfully done.


## Results
- Successfully create a multi-container Docker setup with a web server (Nginx), an application server (Node.js), and a database (MariaDB).
- Verify load balancing by observing different hostnames in the responses from the instances.
- Use `docker-compose ps` to check the status and confirm that all services are running correctly.


## Conclusion
Both challenges were significant learning experiences that deepened my understanding of Docker Compose and container orchestration. It highlighted the importance of environment variables for configuration, the process of building and scaling services, and the benefits of using Docker for local development environments.

## PS
Related screen captures are provided in the Word file for reference
