# Model deployment using FastAPI and Monitoring using Prometheus and Grafana
As part of MLOps, this assignment aims to deploy the ML model on a web server using Fast Api. FastAPI is a modern, fast (high-performance), web framework for building APIs with Python 3.8+ based on standard Python type hints. For keeping the task simple a simple MNIST digit classifier is chosen to serve for this purpose. The API is used in the Swagger UI for checking the model prediction. For monitoring the health of the server Prometheus and Grafana is used. Everything is done in Docker container.
## Description of files and folders
1. ```FastApi_implement.py``` This is the main code file which includes codes for deployment of the model on fastapi. It also contains custom metrics of prometheus to monitor API health.
2. ```MNIST_Model.keras``` is the keras trained model trained on MNIST digit data.
3. ```Dockerfile``` is a text file that contains instructions for building a Docker image. 
4. ```docker-compose.yml``` is the configuration file that is used to define and run multi-container Docker applications. It contains service which is responsible for the creation of the container, we have total 4 containers web1, web2, prometheus, grafana. They also have their respective ports on which their servers will run.
5. ```prometheus.yml``` this .yml file specifies which servers to monitor, for our case it is web1, web2.
6. ```.dockerignore``` file contains name of the files which wont be considered by docker while making the docker image.
7. ```A7 -Dockerize and Monitor FastAPI for MNIST digit prediction.pdf``` contains the problem statement of the assignment.
8. ```result``` contains the screen shots of the prometheus and grafana UI.
9. ```requirements.txt``` contains list of all depedencies
## How to Set up
1. Change directory to the one containing FastAPI_implement.py and MNIST_model.keras.
2. Create Dockerfile in the same directory.
3. Define all the configurations about the container in docker-compose.yml file.
4. To track the fastAPI server create prometheus.yml file.
## Prometheus metrics
## Result of the Dashboard
