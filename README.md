## Introduction

This is a simple Python flask app with a modal chat window for the users to interact with GPT models within an empty web page. The goal of this project was to use GPT-4 available from Bing and gerenate a webpage with dragable modal chat window that would represent an interface for the user to interact with the OpenAI GPT model.

### Frontend

The frontend is written using Bootstrap as well as custom JavaScript to send user's query in the background and receive the response back from the OpenAI GPT model.

### Backend

The backend is written in Python flask with `/chat` and `/` routes to process user's queries.

## Installation

1. Run `pip install -r requirements.txt` to install all necessary dependencies.
2. If Docker is not already installed on your machine, install it. Link for Ubuntu machines https://docs.docker.com/engine/install/ubuntu/, if your distribution is not Ubuntu search the web for the installation guide that fits your machine.
3. Replace the openai_api with your OpenAI API key inside of `app.py` file.
4. Run `flask --app app run --host 0.0.0.0 --debug` from the main directory of this project. (Not needed for Docker) 


## Docker
In order to run the application in a docker container simply follow installation instructions and then run the command `docker compose up` in chatgpt-webapp directory. After completed open up to your localhost on port 5000 and the app will be avalible there!!
