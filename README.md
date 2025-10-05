# per-dev-ops
🐳 What is Docker? (The Core Tool)
Definition: Docker is a platform that allows you to run applications inside a lightweight, isolated box called a Container.

Key Benefits 🎯 (Why we use Docker?)
Consistency/Compatibility: The application runs identically everywhere (eliminating the "works on my machine" problem).

Portability: Containers can run on any major operating system (Windows, Mac, or Linux) without modification.

Speed and Efficiency: Containers are lightweight and start up very quickly.

Key Concepts
Containers: Self-contained, executable software packages that include everything an application needs (code, runtime, libraries, environment variables).

Images: Read-only templates used to create containers.

Docker Compose: A tool for defining and running multi-container Docker applications using a YAML file.

Benefits
Consistency across all environments

Easy isolation of services

Simple deployment and scaling

What is Docker Compose?
Docker Compose is a tool that allows you to run multiple containers simultaneously using a single file called docker-compose.yaml. Instead of running each database or service with lengthy commands, you write them all in a single YAML file(docker-compose.yaml):

Benefit: I don't need to manually operate each database. Docker Compose = container management.



Steps to Install Docker

Steps to Install Docker (สรุปสั้น ๆ):
1 Download: Visit the Docker website and download Docker Desktop for Mac/Windows.
2 Verification: Check installation with docker --version.
3 Test Run: Confirm container capability with docker run hello-world.

The commands used to start and run the Docker application are defined in the docker-compose.yml file.
docker-compose up -d
Once you have saved the docker-compose.yml file in your project folder, open your Terminal and run the following commands:

Navigate to your project directory:

cd /path/to/your/db-stack/
Start all services simultaneously (The Magic Command):
This command downloads the images (if not already present), creates the containers, and runs everything in the background (-d = Detached Mode):

docker-compose up -d
Verify that all containers are running:
You should see all 4 containers (influxdb, postgres, cassandra, jupyter) listed as up and running:

docker ps
Access Jupyter Notebook:
Open your web browser and navigate to the URL, using the Token you defined for secure login:

URL: http://localhost:8888
Token: mytoken123


