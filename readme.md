Bike Share API - Mini Project 1: Simple ML Model Deployment
This repository contains the code for deploying a simple ML model using a pre-trained model and serving predictions through an API endpoint.

Objectives
Deploy a simple ML model using a pre-trained model and serve predictions through an API endpoint.
Implement an API server using a Python web framework like Flask or FastAPI.
Set up a GitHub Actions workflow to automate model testing and deployment on each push to the repository.
Build a Docker container for the API server with the necessary dependencies and the pre-trained model.
Utilize Docker Hub to store the Docker image.
Deploy the Docker container on AWS EC2.
Set up an API Gateway to expose the API endpoint securely.
Steps
Clone the Repository: Clone this Git repository to your local machine.

bash
Copy code
git clone https://github.com/Azim-js/Bike_share_api.git
Set Up Environment: Ensure you have Python installed on your machine. Create and activate a virtual environment using virtualenv or conda.

bash
Copy code
# Example using virtualenv
virtualenv venv
source venv/bin/activate
Install Dependencies: Install the required Python packages by navigating to the project directory and running:

bash
Copy code
pip install -r requirements.txt
Implement API Server: Implement the API server using a Python web framework like Flask or FastAPI. You can find the server code in the repository.

GitHub Actions Workflow: Set up a GitHub Actions workflow to automate model testing and deployment on each push to the repository. Refer to GitHub Actions documentation for setting up workflows.

Build Docker Container: Build a Docker container for the API server with the necessary dependencies and the pre-trained model. Use the Dockerfile provided in the repository.

bash
Copy code
docker build -t bike_share_api .
Docker Hub: Push the Docker image to Docker Hub for easy access and deployment.

bash
Copy code
docker tag bike_share_api your_dockerhub_username/bike_share_api
docker push your_dockerhub_username/bike_share_api
Deploy on AWS EC2: Deploy the Docker container on AWS EC2. You can SSH into your EC2 instance and run the Docker container.

Set Up API Gateway: Set up an API Gateway on AWS to expose the API endpoint securely. Configure the API Gateway to route requests to the EC2 instance where the Docker container is running.

Usage
After deployment, you can access the API endpoint securely through the configured API Gateway URL.
Make POST requests to the API endpoint with input data to get predictions from the ML model.
