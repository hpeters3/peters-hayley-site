### Dockerizing your React app and opening it at 127.0.0.1:7775
To start, navigate to your root directory for the project you want to dockerize (presumably this repository) and run this command:

docker build -t peters-hayley-site .

This will create an image from your Dockerfile. This image lays the foundation for a connection at 0.0.0.0:3000 . However, we don't want that. We also don't want the container to have a random name, so we'll enter this command to create the container:

docker run --name peters-hayley-coding-assignment11 -p 127.0.0.1:7775:3000 peters-hayley-site

It's pretty long, but it does exactly what we want it to. This command will allow you to run your dockerized React app on 127.0.0.1:7775 .
Now you can open your Docker UI and open the port from there, or type 'localhost:7775' in your browser and your React app will pop up.

Happy coding!