# Bash Scripting

With fully established cloud server, DNS and HTTPS connection, bash scripts can be used to automate certain server functions including backing up the server.

This stage of the project covers the developement and implememntation of a basic bash script that logs when the Express.js application starts on run up.

Bash script:

    #! /bin/bash
    
    
    echo "starting node application"
    
    cd /var/testapp
    /usr/bin/npm start > /tmp/testapp.log 2>@1   

