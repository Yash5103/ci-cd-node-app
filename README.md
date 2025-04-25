# CI/CD Node App

This project demonstrates a **CI/CD pipeline** using **GitHub Actions** and **Docker**. The app is a simple Node.js application that is built, tested, and deployed using a fully automated pipeline without the need for cloud infrastructure.

## Features

- **Node.js App**: Simple API that runs on port 3000.
- **Dockerized**: The app is packaged in a Docker container for easy deployment.
- **CI/CD Pipeline**: GitHub Actions is used to automate the build, test, and deployment process.
- **Docker Hub**: The Docker image is pushed to Docker Hub for easy distribution.

## Requirements

- [Docker](https://www.docker.com/)
- [Git](https://git-scm.com/)
- [GitHub](https://github.com/)
- A Docker Hub account

## Setup Instructions

### Clone the Repository

1. Clone this repository to your local machine:
    ```bash
    git clone https://github.com/Yash5103/ci-cd-node-app.git
    cd ci-cd-node-app
    ```

### Run Locally

1. Build the Docker image:
    ```bash
    docker build -t ci-cd-node-app .
    ```

2. Run the Docker container:
    ```bash
    docker run -p 3000:3000 ci-cd-node-app
    ```

3. Open [http://localhost:3000](http://localhost:3000) in your browser. You should see the app running!

### GitHub Actions CI/CD

1. Push your code to the `main` branch of your GitHub repository.
2. GitHub Actions will automatically build and push the Docker image to **Docker Hub**.
3. You can pull the image from Docker Hub and run it anywhere:
    ```bash
    docker pull YOUR_USERNAME/ci-cd-node-app:latest
    docker run -p 3000:3000 YOUR_USERNAME/ci-cd-node-app
    ```

## Project Structure

