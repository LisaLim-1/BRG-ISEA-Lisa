# Virtualisation and Linux Setup

Session 1a: Setting up Ubuntu and Linux on VMware Fusion

In this entry, it will be focused on setting up the virtual machine, loaded with Ubuntu, and connected to the internet. 

<img width="576" height="346" alt="Image" src="https://github.com/user-attachments/assets/f2944a79-5e65-405e-a4bb-a1d4f9b97f8c" />

This is version of VMware Fusion that will be used throughout all labs. 

<img width="1305" height="952" alt="Image" src="https://github.com/user-attachments/assets/da691551-d42f-48ac-96d6-11bb585fe6b8" />

Ubuntu image was sourced from their official website. 

<img width="640" height="525" alt="Image" src="https://github.com/user-attachments/assets/bc62a9ac-66d7-4dba-a339-aeed2d5a7f3b" />

The virtual machine has been set up with the following configurations. 


<img width="639" height="423" alt="Image" src="https://github.com/user-attachments/assets/f3e26f55-6dca-41b7-acfb-ae38578d0e0d" />

Bridged Network has been set up between the virtual machine and host device.

<img width="1288" height="771" alt="Image" src="https://github.com/user-attachments/assets/5449b33d-f7c2-414a-ba50-7226d07bc06b" />

Internet connection has been established successfully from host device to virtual machine. 

<img width="1288" height="542" alt="Image" src="https://github.com/user-attachments/assets/0f809913-8d3f-485d-ac9f-4b69ddc78b46" />

Terminal has been successfully booted up upon installation of Ubuntu and rebooting the virtual machine. 

<img width="858" height="471" alt="Image" src="https://github.com/user-attachments/assets/e137eb1e-787c-41d4-a2bf-9cd1ca642886" />

Completion of packages being updated after running 'sudo apt update -y' and 'sudo apt upgrade -y'

1. sudo grants administrative privileges to perform the required actions (in this case would be updating and upgrading of packages). 

2. apt refers to Ubuntu's package management system that will manage the installation, upgrading and removal of software. between update and upgrade, I noticed that update refers to pulling out what are the new available packages for download whereas upgrade would perform the actual download of the packages and hence takes a longer time to complete. 

3. -y in this case references to indicating 'YES" during the confirmation sought from the system. 
