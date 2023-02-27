# Week 1 — App Containerization

## Containerized Application (Dockerfile and Docker compose)

After creating a new github repo and  launching it within a new gitpod space
Firstly i installed dockerfile on the backend
On the backend file, I entered the code to run python
I opened the port  for 4567 and ran on my browser and appended /api/activities/home ro my URL to launch the browser


## Adding Dockerfile

Still on the backend, I opened a new Dockerfile and pasted the docker configuration

I typed in _pip3 install -r requirements.txt _ to run flask and set the environment variables export FRONTEND_URL="*"
export BACKEND_URL="*" to start it up

I opened the port it got running on port 4567 

## Build Container

I pasted _docker container run --rm -p 4567:4567 -d backend-flask_ to run the container image

While container image is running, curl was sent to test the server _curl -X GET http://localhost:4567/api/activities/home -H "Accept: application/json" -H "Content-Type: application/json"


## Containerize Frontend

NPM was installed on the frontend using cd _frontend-react-js_
_npm i_
I created another dockerfile on the frontend and pasted the code 
I created a docker-compose file to run multiple containers

## Adding Postgrel and Dynamodb

Finally I intergrated postgrel and dynamodb into my docker compose file

