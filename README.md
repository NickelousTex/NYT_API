# NYT_API
NYT API dict flattening

We will use a docker container to ensure ability to recreate the enviroment. We'll use Python 3.8 for the exercise. 

### Docker setup

Install and run the newest Docker for Mac.

The Docker image that we will be building and using is based on the official python version of buster-slim.
    
### Using Docker

Next, navigate to the ```squirro``` repo directory where there is a ```Dockerfile_buster_slim``` and a ```docker-compose.yml``` (also where these instructions live).  Here you will build out the services:

    docker-compose build

Then, to start up the development container, type the following command:

    docker-compose up -d

The container runs in the background.  To access the ```python 3.8``` enviroment (named ```py3```) to run tests, etc., use this command:

    docker-compose exec dev bash

You can exit the container with ```exit``` and go back in again later with the previous command.

The simple way to shut the whole environment down with one command is to use:

    docker-compose rm -sf

This will stop the containers and delete them.  Keep in mind that any changes inside the containers will be lost at that point.  This does not affect the code in the repo, as it is mounted *inside* the container from your local machine.

To get up and running again, use the 

    docker-compose up -d
