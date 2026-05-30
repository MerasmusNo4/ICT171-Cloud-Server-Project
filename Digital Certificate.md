# Digital Certificate

Now that the cloud server is easily accessible through DNS, connection to the server can be made more secure by enabling connection through the server's HTTPS port instead of it's HTTP port. This can be acheived by downloading a digital certificate from an appropriate SaaS.

This stage of the project covers downloading a digital certificate from Certbot and installing and configuring it on the cloud server to enable connection through HTTPS.

## Download and install Digital Certificate using Certbot:

Go to the Certbot website:
[https://certbot.eff.org](https://certbot.eff.org)

Under the query "what's your http website running on?" select "Nginx" and "Linux (pip)

Follow all the steps on your cloud server up to step 7.

For step 7, choose to get and install your certificate over the other option:

    sudo certbot --nginx


### Reboot Nginx:

After following these steps, remember to reboot nginx:

    sudo systemctl restart nginx

Then, check to see if nginx is running:

    sudo systemctl status nginx

Nginx may need to be enabled and started after the reboot:

    sudo systemctl enable nginx
    sudo systemctl start nginx

Now, the cloud server can be accessed through:

    https://aicentral-asimovss.tech

If not, remember to check if port 443 is open through the firewall, ad open it if it isn't:

    sudo ufw status verbose
    sudo ufw enable 443/tcp
