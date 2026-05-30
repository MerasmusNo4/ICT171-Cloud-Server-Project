# Local Virtualisation

Before creating the cloud server, an Ubuntu Linux environment must be established. The initial installation, configuration and maintenance of server software will be managed from this environment. 

This step covers the download and installation of the virtualisation software 'Virtualbox' alongside the download and installation of Ubuntu itself.

### Important Note:

If you already have access to a CLI that can run Bash, such as the Windows or Mac Terminals, this section is optional.

A vast majority of this project was completed using the Mac Terminal and not a local virtual machine.

## Download and Install Virtualbox and Ubuntu

### Start by downloading installing Virtualbox:

This can be done from the link below:
[https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

Open the .dmg and follow the steps to install Virtualbox before preceding. 

### Then Download Ubuntu:

Download the latest version of Ubuntu ~~(Ubuntu 24.04 LTS)~~ (Ubuntu 26.04 LTS) from the link below. 

[https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

Windows users should download the "AMD" version, while macOS users should select the "ARM" version.
Much like with Virtualbox, open the .dmg and complete the installation process before proceding.

## Set up an Ubuntu Linux Virtual Environment:

Follow these steps:

1. Start Virtualbox
2. Create a new virtual machine
3. Call the machine "ubuntu", put the downloaded iso file into iso selection and uncheck unattended install
4. Enter the following configurations:
    - 4096 MB memory
    - 2 core
    - Change the scale factor to 230%
5. Leave everything else as default
6. Click start
7. Virtual Box will tell you that you are starting a machine with no boot media. You need to point Virtualbox towards your Ubuntu .iso file so that it can boot from this

After following these, steps, the following windows should look like this:

![Virtualbox](https://github.com/MerasmusNo4/ICT171-Cloud-Server-Project/upload/main)                  ![](ubuntu)



