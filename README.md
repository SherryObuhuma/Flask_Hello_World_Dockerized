# Flask Web Application (Dockerized)

A simple Flask web app containerized with Docker and served using Gunicorn. Built as a starter project to practice deployment basics.

---

# Prerequisites
- Install [Docker](https://docs.docker.com/get-docker/) on your machine.
- Make sure port **5000** is free (the app will run on it).

--- 

## Build the Docker Image
From the project root where the Dockerfile is located, run:

```bash
docker build -t myflask_img:v1.0.0 .
```
---

## Run the container
Start the container in detached mode and expose port 5000:

```bash
docker run -d --name myflask_app -p 5000:5000 myflask_img:v1.0.0
```
---

## Access the Application
Once the container is running, open your browser and go to:

http://localhost:5000/

----

## View Logs

```bash
docker logs myflask_app
```

---

## Stop and Remove the Container
To stop the app: 

```bash
docker stop myflask_app
```

To remove it completely:

```bash
docker rm myflask_app
```

---



