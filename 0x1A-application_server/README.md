![app](https://github.com/itodoemmanuel/alx-system_engineering-devops/assets/54606115/ba94dee8-a03e-4604-ad1d-ed72a7889587)
Your web infrastructure is already serving web pages via Nginx that you installed in your first web stack project. While a web server can also serve dynamic content, this task is usually given to an application server. In this project you will add this piece to your infrastructure, plug it to your Nginx and make is serve your Airbnb clone project.

Project Requirements
A README.md file, at the root of the folder of the project, is mandatory
Everything Python-related must be done using python3
All config files must have comments
All your files will be interpreted on Ubuntu 16.04 LTS
All your files should end with a new line
All your Bash script files must be executable
Your Bash script must pass Shellcheck (version 0.3.7-5~ubuntu16.04.1 via apt-get) without any error
The first line of all your Bash scripts should be exactly #!/usr/bin/env bash
The second line of all your Bash scripts should be a comment explaining what is the script doing.
Project task
Set up development with Python Let’s serve what you built for AirBnB clone v2 - Web framework on web-01. This task is an exercise in setting up your development environment, which is used for testing and debugging your code before deploying it to production.
Requirements:

Make sure that task #3 of your SSH project is completed for web-01. The checker will connect to your servers.
Git clone your AirBnB_clone_v2 on your web-01 server.
Configure the file web_flask/0-hello_route.py to serve its content from the route /airbnb-onepage/ on port 5000.
Your Flask application object must be named app (This will allow us to run and check your code).
Solving task 0
git clone Airbnb_clone_v2
edit the file 0-hello_route.py by replacing "/" with "airbnb_onepage"
(venv) ubuntu@64820-web-01:~/AirBnB_clone_v2$ python3 -m web_flask.0-hello_route
 * Serving Flask app '0-hello_route'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:5000
 * Running on http://10.247.26.30:5000
Press CTRL+C to quit
127.0.0.1 - - [10/Feb/2023 21:00:05] "GET /airbnb-onepage HTTP/1.1" 200 -
After Fixing

ubuntu@64820-web-01:~$ curl localhost:5000/airbnb_onepage
Hello HBNB!ubuntu@64820-web-01:~$
