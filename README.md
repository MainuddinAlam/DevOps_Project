# Final Project of the Shiftkey DevOps course
### Submission by - **Mainuddin Alam Irteja**

## Project Overview
Welcome to my final project of the Shiftkey DevOps Foundations course. The overview of this project was to gain valuable experience in implementing Docker containers with CI/CD pipeline so that I was able to run the given calulator project. 

### Main Implemented files
* Backend Dockerfile in the backend directory
* Frontend Dockerfile in the frontend directory
* Docker-compose.yml file to run the multi-container Calculator application
* The github-actions.yml file to build, test and deploy the application
* A README.md file to document my progress

## Docker Implementation
#### Backend Dockerfile:
The backend Dockerfile builds the Flask app needed to perform mathematical calculations that the frontend calculator app needs. My backend Dockerfile successfully builds the Flask backend application. Steps to run the backend Docker file on its own is given below:-
* Clone my repository and ensure docker is installed in your local machine
* Open up a terminal and go to the backend directory of my repository
* Run the following in the terminal
* docker build -t py-app .    
* docker run -p 4000:4000 py-app  

#### Frontend Dockerfile:

#### Docker-compose.yaml file:

#### github-actions.yml file


