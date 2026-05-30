# Node.js and Express.js

Now that the static component of the cloud server is up and running through Wordpress, it's time to construct a basic demo of a web application. The development software, Node.js, and one of its extensions, Express.js have been chosen for this task.

This stage of the project covers the local installation of Node.js and Express.js and their installation on the cloud server. This stage also covers the installation of the Express Application Genarator, an Express tool that provides developers with the basic skeleton of a web application that can be easily customised and expanded upon. 

In this way, Node.js and Express.js will be used to develop and display the prototype for an interactive web app which will provide the cloud server's core AI central functionality. 

Node.js was chosen over other software due to it's ability to handle massive numbers of concurrent connections, an extermely useful feature for AI Central which has been designed to connect to a wide variety of AI software.

Useful Website:
[https://www.w3schools.com/nodejs/nodejs_express.asp](https://www.w3schools.com/nodejs/nodejs_express.asp)

How to run the application automatically:

First, run:

    sudo nano /etc/systemd/system/my-node-app.service

Then, write the following program (bash script must have been completed beforehand):

    [Unit]
    Description=My Node.js App
    After=network.target

    [Service]
    ExecStart=/usr/bin/bash /var/testapp/runapp.bash
    WorkingDirectory=/var/testapp
    Restart=always
    RestartSec=10
    Environment=NODE_ENV=production
    User=root
    Group=root
    StandardOutput=syslog
    StandardError=syslog
    SyslogIdentifier=my-node-app

    [Install]
    WantedBy=multi-user.target


