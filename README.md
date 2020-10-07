# Deploying a Flask API

## Endpoints
##### `GET '/'`: This is a simple health check, which returns the response 'Healthy'. 
##### `POST '/auth'`: This takes a email and password as json arguments and returns a JWT based on a custom secret.
##### `GET '/contents'`: This requires a valid JWT, and returns the un-encrpyted contents of that token. 

The app relies on a secret set as the environment variable `JWT_SECRET` to produce a JWT. The built-in Flask server is adequate for local development. For production use  [Gunicorn](https://gunicorn.org/) server when deploying the app.

## Dependencies

- Docker Engine
    - Installation instructions for all OSes can be found [here](https://docs.docker.com/install/).
    - For Mac users, if you have no previous Docker Toolbox installation, you can install Docker Desktop for Mac. If you already have a Docker Toolbox installation, please read [this](https://docs.docker.com/docker-for-mac/docker-toolbox/) before installing.
 - AWS Account
     - You can create an AWS account by signing up [here](https://aws.amazon.com/#).