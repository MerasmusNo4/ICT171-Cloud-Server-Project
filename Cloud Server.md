# Cloud Server

Now that an Ubuntu desktop has been set up on VirtualBox, the cloud server can now be established. For this project, the server will be run on another virtual machine purchased from IaaS. Then, web server software must be installed on the virtual machine. After this step, a webpage can be created and modified with HTML code.

This stage of the project covers the purchase and configuration of a virtual machine from the Microsoft Azure. It will also cover the installation of nginx from the Ubuntu desktop and initial HTML modifications.

## Create the Cloud Server

Navigate to Microsoft Azure using this link: [https://portal.azure.com/#home](https://portal.azure.com/#home)

After logging in, click on "Virtual Machines" and then click create > Virtual Machines.

Enter the following configurations (anything not listed should be left as default):

- **Subscription** -> Azure for Students
- **Resource group** -> Create new > Name: "WebServer_Resources"
- **Virtual machine name** -> "AICentral-Proposal"
- **Region** -> (Asia Pacific) Australia east
- **Image** -> Ubuntu Server 24.04 LTS - x64 Gen2
- **VM Architecture** -> x64
- **Size** -> Standard_B2als_v2
- **Authentication Type** -> SSH public key
- **Username** -> "Merasmus06"
- **SSH public key source** -> Generate new key pair
- **Key pair name** -> "Webserver_key"
- **Public inbound ports** -> Allow selected ports
- **Select inbound ports** -> []SSH (22), []HTTP (80), []HTTPS (443)

Then, click on "Review + create" and then "Create" and the server should start.
The SSH public key can be downloaded from Azure.

## Connect to Cloud Server:

The server ca be remotely connected to on a local device through the macOS terminal.
Open the macOS terminal, navigate to the directory with the SSH public key, and enter the following command:

    ssh -i "Webserver_key.pem" Merasmus06@[server_ip_address]

The server's public IP address can be found on the server's "Overview" page

