# Read:31 - Django REST Framework & Docker - 03/15/2022

- Docker: a way to isolate and run entire application. The entire development environment is isolated: programming language, software packages, databases, and more.
- Useful Docker command
  - docker --version
  - docker-compose --version
  - docker run hello-world
  - docker info
  - docker image ls
  - docker container ls -la
  - docker image build .
- Docker summary
  - Docker is a way to run Linux container
  - Containers are a lightweight alternative to Virtual Machines
  - `Dockerfile` is a list of instructions for creating an image
  - Images are made up of one or more layers
  - Containers are a running instance of an image
  - `docker-compose.yml` controls how to run the container
  - Containers are stateless and ephemeral in nature. We can link the local filesystem via `volumes` but things become more complex with databases
