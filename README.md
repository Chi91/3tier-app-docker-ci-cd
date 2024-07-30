# Deployment of Sample Application with CI/CD Pipeline

This project involves deploying a sample application with a backend built using .NET Core, a frontend built with HTML, CSS, and JavaScript, and a PostgreSQL database. A CI/CD pipeline is created using GitHub Actions to automate the deployment process.

## Application Overview

The sample application includes the following components:

- **Backend Application**: Built with .NET Core.
- **Frontend Application**: Built with HTML, CSS, and JavaScript.
- **Database**: PostgreSQL.

## CI/CD Pipeline with GitHub Actions

The GitHub Actions pipeline automates the following steps:

1. **Build, Test, and Scan Code**: Build the application, run tests, and perform a security scan.
2. **Create Docker Images**: Build Docker images for both the frontend and backend applications.
3. **Push Docker Images to DockerHub**: Push the Docker images to DockerHub as new versions.

Additionally, the pipeline handles deployment to an EC2 instance:

1. **Connect to EC2 Instance**: Add steps to connect to the EC2 instance where Docker is installed.
2. **Pull Docker Images**: Pull the frontend and backend images from DockerHub that were pushed in the previous steps.
3. **Run Docker Containers**: Run the Docker images as containers on the EC2 instance.


The workflow configuration can be found in `.github/workflows/deploy.yml`. Below is a general overview of the steps included:


