### Dockerizing your React app and opening it at 127.0.0.1:7775

By default, the app will open on 3000, and the dockerized default is 0.0.0.0:3000 .
This is okay when you're creating the image. In your root directory, run:

docker build -t peters-hayley-site .

This will create the image for your docker file. Now, when you create the container, you need to change where Docker will run. For that, run this command:

docker run -p 127.0.0.1:7775:3000 peters-hayley-site

This will allow you to run your dockerized React app on 127.0.0.1:7775 .
Now you can open your Docker UI and open the port from there, or type 'localhost:7775' in your browser and your React app will pop up.

Happy coding!