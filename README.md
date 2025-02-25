# Overview

This repo provides a Dockerized setup for deploying a Flask web application using PostgreSQL, Gunicorn, and Nginx. In development, the setup uses Flask's built-in server, but in production it uses Gunicorn as the WSGI server and Nginx as a reverse proxy. 

# Successful Uploading of "successful.jpeg" Image in Production
![Successful image upload](./success_image_upload.gif)


# Build Instructions
## Development
You can build and start the containers by running this command:
```
docker compose up -d --build
```
You can now access the application at http://localhost:9090. For development, the code changes apply automatically as the "web" folder is mounted into the container. 

## Production
You can build and start the containers by running this command:
```
docker compose -f docker-compose.prod.yml up -d --build
```
You can now access the application at http://localhost:1351. For production, no folders are mounted, so in order to make changes, you must rebuild the image using the above command. 

Happy building :)
