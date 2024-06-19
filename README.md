# Flow CRM

This project is a Vaadin application created with Spring Boot.
It contains all the necessary configuration.

## Running the application

The project is a standard Maven project. To run it from the command line,
type `mvnw` (Windows), or `./mvnw` (Mac & Linux), then open
http://localhost:8080 in your browser.

## Project structure

- `MainLayout.java` in `src/main/java` contains the navigation setup (i.e., the
  side/top bar and the main menu). This setup uses
  [App Layout](https://vaadin.com/docs/components/app-layout).
- `views` package in `src/main/java` contains the server-side Java views of the application.
- `views` folder in `src/main/frontend` contains the client-side JavaScript views of the application.
- `themes` folder in `src/main/frontend` contains the custom CSS styles.


## Deploying using Docker

To build the Dockerized version of the project, run

```
mvn clean package -Pproduction
docker build . -t my-app:latest
```

Once the Docker image is correctly built, you can test it locally using

```
docker run -p 8080:8080 my-app:latest
```
