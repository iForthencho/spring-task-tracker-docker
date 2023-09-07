# spring-task-tracker

Task tracking application to showcase a simple RESTful API using Java and Spring Boot.

### Features

- CRUD operation for tasks
- Basic user/endpoint authentication using Spring security
- Endpoint error handling

### Prerequisites

- Docker

### Setting Up

1. Clone the repository:
<br><br>
    ```
    git clone https://github.com/iForthencho/spring-task-tracker-docker.git
    cd spring-task-tracker-docker
    ```
2. Build the jar file
<br><br>
   ```
   ./mvnw package
   ```
3. Build the Docker image:
<br><br>
   ```
   docker build -t dockertasktracker .
   ```

4. Run the container
<br><br>
   ```
   docker-compose up
   ```
   The app will be accessible at "http://localhost:8080".

### API Endpoints
| HTTP Method | Endpoint | Description |
| --- | --- | --- |
| GET | /api/tasks | List all tasks |
| GET | /api/tasks/{id} | Retrieve a task by ID |
| POST | /api/tasks | Create a new task |
| PUT | /api/tasks/{id} | Update a task by ID |
| DELETE | /api/tasks/{id} | Delete a task by ID |

### User Authorization
* Please note that this is just to showcase spring security, hence usernames and passwords are added here.
* BCrypt encryption is used in this demo.

| Username | Password | Role                     |
| --- |---|--------------------------|
| shawn | daintern | EMPLOYEE, MANAGER, ADMIN | 
| susan | daintern | EMPLOYEE, MANAGER |
| john | daintern | EMPLOYEE |


