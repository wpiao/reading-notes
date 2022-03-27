# Retro:34 - Backend Deployment - 03/26/2022

**Deploy django app to the AWS**

1. Create an AWS instance and log into the instance.
2. Add `TCP, 8000, 0.0.0.0/0` to the inbound rule.
3. Install `git` and `docker` and `docker-compose` in the instance.
4. Clone down the repo and create `.env` file inside the `project` folder.
5. Run command `docker-compose run web python manage.py collectstatic` to create static folder/files.
6. Run command `docker-compose up --build` to build the container.
7. Debug as needed.
