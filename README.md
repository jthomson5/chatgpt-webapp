## Introduction

This is a simple Python flask app with a modal chat window for the users to interact with GPT models within an empty web page. The goal of this project was to use GPT-4 available from Bing and gerenate a webpage with dragable modal chat window that would represent an interface for the user to interact with the OpenAI GPT model.

### Frontend

The frontend is written using Bootstrap as well as custom JavaScript to send user's query in the background and receive the response back from the OpenAI GPT model.

### Backend

The backend is written in Python flask with `/chat` and `/` routes to process user's queries.

## Installation

1. Run `pip install -r requirements.txt` to install all necessary dependencies.
2. If Docker is not already installed on your machine, install it. Link for Ubuntu machines https://docs.docker.com/engine/install/ubuntu/. If your distribution is not Ubuntu search the web for the installation guide that fits your machine.
3. Replace the openai_api with your OpenAI API key inside of `app.py` file.
4. Run `flask --app app run --host 0.0.0.0 --debug` from the main directory of this project. (Not needed for Docker) 


## Docker
1. In order to run the application in a docker container first simply follow the installation instructions. Step 3 will not be needed if you plan on only running the app in a docker container.
2. If Docker is not already installed on your machine, install it. Link for Ubuntu machines https://docs.docker.com/engine/install/ubuntu/. If your distribution is not Ubuntu search the web for the installation guide that fits your machine.
3. This docker container runs on port 5000 on your localhost, so if another running conatiner is also using port 5000 make sure to stop that conatiner. To check if there are any other running containers using port 5000 use the `docker ps` command to see all other running conatiners and the ports they are running on. If there is another container using port 5000 use the `docker stop <ID>` command using the ID of the container found in the previous command to stop the container entirely or change the ports on the conflicting container if possible.
4. Once the following steps have been completed use the `docker compose up` command in the chatgpt-webapp directory created when cloning this repo, then go to your browser of choice and type in the IP adress of either your local host or VM followed by :5000 to be directed to the app running in a docker container.
