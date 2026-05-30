# DNS

For easier access to the newly established cloud server, a domain must be purchased from the appropriate SaaS and a domain name linked to the server's public IP address. 

This stage of the project covers the purchase of the domain ".tech" from Namecheap and linking the domain name "aicentral-asimovss.tech" to the server's IP address.


## Check Firewall

Before setting up DNS, check that the cloud server's firewall is up and running. Use:

    sudo ufw status verbose

If the firewall is off, enable it using:

    sudo ufw enable

Then run "status verbose" once more. It should display ports 22, 80 and 443 as open. Then, enter the folowing command:

    sudo ufw allow 3000/tcp

This should open port 3000, which will be vital for implementing the Express.js web application demo later on in the project.

# Purchase & Link a Domain Name:

Next up: purchasing a domain name from Namecheap.

Firstly, go to the site using this link:
[https://www.namecheap.com](https://www.namecheap.com)

For this project, search for the domain name ".tech". After purchasing the domain name, navigate to "Domain list" > the domain just purchsed > "Advanced DNS" and follow these steps:

1. **Add a new record**:
    - **Type** -> A Record
    - **Host** -> "@"
    - **IP Address** -> "IP address of cloud server"
    - **TTL** -> Automatic
3. **Add another new record**:
    - **Type** -> CNAME Record
    - **Host** -> "www"
    - **Target** -> "aicentral-asimovss"
    - **TTL** -> Austomatic

Now, connection to the server can be acheived by entering:

    http://aicentral-asimovss.tech


