# My first project using Docker and NGINX

Super simple Nginx reverse proxy setup for an express app.

There are two containers running:
- Express (dockerfile: express.Dockerfile)
- nginx (dockerfile: nginx.Dockerfile)

Docker compose automatically configures a network

## How to run
1. run docker compose up -d
2. Both NGINX and Express containers should run. Run docker ps and check
3. Go to localhost (nginx is running on port 80)
4. Ensure the page loads. The content should be the same as index.ejs found in the /views directory
4. Go to the network tab and refresh the page. Check the response section and look for the server header. The value should nginx.

## What i learned
- Simple nginx reverse proxy set up
- Dockerizing an express app
- Dockerizing nginx
- Writing a docker compose file