[![ismailukman](https://circleci.com/gh/ismailukman/operationalize-ml-microservice.svg?style=svg)](https://app.circleci.com/pipelines/github/ismailukman/operationalize-ml-microservice)



## Project Overview

This Microservice is part of the Operationalize Machine Learning project prepared from Scikit-Learn . It includes a model that forecasts Boston home values based on a number of characteristics, including the typical number of rooms in a home and information on highway accessibility, teacher-to-student ratios, and other factors. You may read more about the data on [the data source site] (https://www.kaggle.com/c/boston-housing), which was where the original Kaggle data came from.

## What does this project do?

- Prepare the environment
- Run a docker container
- Upload container into a public registry (hub.docker.com)
- Run the deployed application in a Kubernetes cluster
- Integrate with CircleCI for continuous integration

## Requirements
 - Python 3.8.10

## START HERE
 - To regenerate the same result, follow the steps below

### Step 0
- Fork this repo and clone my project to your local workstation for your specific project
### Step 1: Install dependencies
- 
- Set up the environment by running `make setup`. This will create a virtual environment in your home directory called `.devops`
- Install dependencies by running `make install`
- (Optionally) Lint application (requires hadolint)

### Step 2: Run Docker container
- Run the application on docker by calling `./run_docker.sh`

### Step 3: Upload to Docker Hub
- In the `./upload_docker.sh` file, edit the dockerpath (line 8) and change the docker username to a personalized one (or leave it as is, to use the public kcemenike/microproject:v1.0.0)
- To upload to docker hub, run `./upload_docker.sh`

### Step 4: Kubernetes deployment
- To deploy to kubernetes, run `./run_kubernetes.sh`

### Step 5: Check status and report success
- current output txt files are found in `output_txt_files`