# Basic Web Application with Docker

## 📌 Project Overview

This project demonstrates how to build and containerize a basic Flask web application using Docker.

The application is developed using Python and Flask, packaged into a Docker image, and executed inside a Docker container.

The project also demonstrates basic Git and GitHub usage for version control and project documentation.

---

## 🎯 Project Objective

The main objective of this project is to understand the fundamentals of Docker and learn how to:

- Create a basic Flask web application
- Create a Dockerfile
- Containerize a Flask application
- Build a Docker image
- Run an application inside a Docker container
- Map container ports to the host machine
- Check running containers
- View container logs
- Stop and start containers
- Use Git for version control
- Push the project to GitHub

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Programming language |
| Flask | Web application framework |
| Docker | Application containerization |
| Git | Version control |
| GitHub | Source code repository |
| PyCharm | Development environment |

---

## 📂 Project Structure

```text
docker-flask-app/
│
├── app.py
├── requirements.txt
├── Dockerfile
├── README.md
└── .gitignore

---

## File Description

app.py - Contains the Flask web application code.
requirements.txt - Contains the Python dependencies required by the application.
Dockerfile - Contains instructions to build the Docker image.
README.md - Contains project documentation and setup instructions.
.gitignore - Specifies files and folders that should not be tracked by Git.


🐍 Flask Application

The Flask application provides a simple web page.

When the application is running, it displays:

Hello! My Flask Application is Running Inside Docker.

The application runs on port:5000


🐳 Dockerfile

The Dockerfile used in this project:

FROM python:3.11-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY app.py .

EXPOSE 5000

CMD ["python", "app.py"]

## Dockerfile Explanation

FROM - Uses Python 3.11 as the base image.
WORKDIR - Sets /app as the working directory inside the container.
COPY - Copies application files into the container.
RUN - Installs the required Python dependencies.
EXPOSE - Documents that the application uses port 5000.
CMD - Starts the Flask application when the container runs.


🚀 How to Run the Project

Step 1: Build the Docker Image
docker build -t flask-docker-app .
Step 2: Check the Docker Image
docker images
Step 3: Run the Docker Container
docker run -d -p 5000:5000 --name flask-container flask-docker-app
Step 4: Check the Running Container
docker ps
Step 5: Open the Application

# Open a web browser and visit:

http://localhost:5000

The application displays:

*Hello! My Flask Application is Running Inside Docker.*

🔍 Docker Commands Used

1.List Docker Images
            docker images
2.List Running Containers
            docker ps
3.List All Containers
            docker ps -a
4.View Container Logs
            docker logs flask-container
5.Stop the Container
            docker stop flask-container
6.Start the Container
            docker start flask-container


🔄 Application Workflow

Developer
    ↓
Flask Application
    ↓
Dockerfile
    ↓
Docker Build
    ↓
Docker Image
    ↓
Docker Container
    ↓
Port Mapping
    ↓
Browser
    ↓
http://localhost:5000


🔧 Git and GitHub

Git was used for version control and GitHub was used to store the project repository.

1.Initialize Git
       git init
2.Add Files
       git add .
3.Create a Commit
       git commit -m "Initial Docker Flask application"

4.GitHub Repository
https://github.com/shivani-bhosle/docker-flask-app

🧪 Testing

The application was tested by:

1.Building the Docker image successfully.
2.Running the Docker container.
3.Checking the container using docker ps.
4.Accessing the application through http://localhost:5000.
5.Checking application logs using docker logs.
6.Stopping and restarting the container.
7.Verifying that the application was accessible after restarting.

✅ Project Result

The Flask web application was successfully containerized using Docker and deployed inside a Docker container.

The application is accessible through:

http://localhost:5000

The project was also version-controlled using Git and uploaded to GitHub.

📚 Key Learning Outcomes

Through this project, I learned:

Flask application basics
Docker fundamentals
Dockerfile creation
Docker image creation
Docker container management
Port mapping
Container logs
Container lifecycle management
Git basics
GitHub repository management
Project documentation



