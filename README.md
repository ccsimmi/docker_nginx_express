# My first project using Docker and NGINX

Super simple Nginx reverse proxy setup for an express app and react app.

There are three containers running:
- Express (dockerfile: express.Dockerfile)
- nginx (dockerfile: nginx.Dockerfile)
- frontend (a react app)

Docker compose automatically configures a network

## How to run
1. run docker compose up -d
2. NGINX, Express and react containers should run. Run docker ps and check
3. Go to localhost (nginx is running on port 80)
4. Ensure the page loads. The content should be the same as index.ejs found in the /views directory
5. Go to the network tab and refresh the page. Check the response section and look for the server header. The value should nginx.
6. Go to /frontend, where the react app is being served

## What i learned
- Simple nginx reverse proxy set up
- Dockerizing an express app
- Dockerizing nginx
- Writing a docker compose file
- Dockerizing a react app scaffolded with vite
- Using NGINX to serve a react app in a subdomain