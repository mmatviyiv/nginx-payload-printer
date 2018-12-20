# Purpose

A quick way to run mock server which prints request body

# Instructions

1. Start nginx container and echo the log forcely

  ```bash
  docker logs -f `docker run -p 8080:80 -d mmatviyiv/nginx-payload-printer:latest`
  ```

2. Post the test data to the nginx server

  ```bash
  curl -X POST http://0.0.0.0:8080/post -d 'test'
  ```
