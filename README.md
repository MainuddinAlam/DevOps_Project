# Final Project of the Shiftkey DevOps course
### Submission by - **Mainuddin Alam Irteja**

## Project Overview
Welcome to my final project of the Shiftkey DevOps Foundations course. The overview of this project was to gain valuable experience in implementing Docker containers with CI/CD pipeline so that I was able to run the given calulator project. 

#### Main Implemented files
* Backend Dockerfile in the backend directory
* Frontend Dockerfile in the frontend directory
* Docker-compose.yml file to run the multi-container Calculator application
* The github-actions.yml file to build, test and deploy the application
* A README.md file to document my progress

## Docker Implementation
#### Backend Dockerfile:
The backend Dockerfile builds the Flask app needed to perform mathematical calculations that the frontend calculator app needs. My backend Dockerfile successfully builds the Flask backend application and I was ablt to test it using the frontend application. Steps to run the backend Docker file on its own is given below:-
* Clone my repository and ensure docker is installed in your local machine
* Open up a terminal and go to the backend directory of my cloned repository
* Run the following in the terminal
* docker build -t py-app .    
* docker run -p 4000:4000 py-app  

#### Frontend Dockerfile:
The frontend Dockerfile builds the React calculator app to perform mathematical calculations. My frontend Dockerfile successfully builds the React frontend application and I was ablt to test it using the backend application. Steps to run the frontend Docker file and test it with the backend:-
* Clone my repository and ensure docker is installed in your local machine
* Start the backend application as mentioned in the Backend Dockerfile section of README.md file
* Open up a terminal and go to the frontend directory of my cloned repository
* Run the following in the terminal
* docker build -t react-app .    
* docker run -p 3000:3000 react-app    

#### Docker-compose.yaml configuration file:
My Docker-compose.yaml successfully builds the Frontend and Backend Dockerfiles and runs them as its services. Hence the frontend calculator application performs the mathematical operations successfully using the backend Flask code. I use a bridge network between frontend and backend containers. Steps to run the Docker-compose.yaml file:-
* Clone my repository and ensure docker is installed in your local machine
* Open up a terminal and go to the cloned directory containing docker-compose.yaml file
* Run the following in the terminal
* docker-compose up

#### github-actions.yml file for CI/CD pipeline
The github-actions.yml file implements the CI/CD pipeline needed to build, test and deploy the application. Pushing code and pull requests triggers the pipeline. My CI/CD pipeline first builds the frontend React application and tests it. Then it builds the backend Flask application and tests it. After the frontend and backend jobs the complete, the github-actions moves on to push the images to a repository of my Docker hub account. The Docker hub repository will have the frontend and backend Docker images which one can use to run them. 

Finally, my github-actions.yml file will deploy the updated code to Render. I have used Github secrets so that I can push images to Docker hub and deploy code to Render. I have given links to my Docker Hub repostiory containing the images and the calculator application hosted on render. The Calculator application maybe a bit slow to load because I am using free tier.
* Docker hub link:- https://hub.docker.com/repository/docker/main71/devops-final-project/general
* Calculator app on Render:- https://frontend-irteja.onrender.com/

## Assumptions
* Users wanting to test out the code need Docker in their local machine
* The CI/CD pipeline should be able to build, test and deploy my application when I push my updated code on my Github repo.

## Lessons Learned
* Gained experience working with Dockerfiles and docker-compose.yml
* Implementing CI/CD pipeline to deploy code was cool
* These will help me with future projects

## Future Improvements
* I would like to make sure the CI/CD pipelint to implement triggers only when github-actions.yml file changes. Right now pipeline triggers when pushing code.
* Maybe include environment variables in Dockerfiles and docker-compose.yaml file