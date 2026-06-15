# Lab 1a Virtualisation and Linux Setup

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

<img width="858" height="471" alt="Image" src="https://github.com/user-attachments/assets/abcc7753-6ca5-46ff-aece-63326275240a" />

Upon completion of installing all updates to the packages, I ran pwd to check which is the current directory I was working in. Subsequently, I used ls to show me what files are currently in the directory I was working from. This helps me to better understand if I would prefer working in the current file or perform any changes in other files instead. 

<img width="858" height="471" alt="Image" src="https://github.com/user-attachments/assets/9066fecb-2ec7-4bcd-8785-ad2794083c14" />

Using ip a, I was able to have a glance of my current network configuration. 

<img width="858" height="471" alt="Image" src="https://github.com/user-attachments/assets/a94b48eb-faf2-4ce1-a648-841283878bc3" />

Without opening the browser, I was able to check on my virtual machine's connectivity to the Internet by running ping -c 4 google.com. By indicating 4 within this line of code, it would only ping to the destination (google.com) 4 times. If there was no command of how many times ping should be carried out, it would continue endlessly. 

<img width="858" height="471" alt="Image" src="https://github.com/user-attachments/assets/582a7c94-d33f-46bd-afde-9277a5ef288d" />

Next I updated and upgraded ssh to ensure that I could remotely connect to another computer or cloud server securely over an unsecured network should it ever be used. 

<img width="858" height="471" alt="Image" src="https://github.com/user-attachments/assets/0ac03858-dbae-46fd-aa90-1102d797d1c2" />

In the screenshot above, I ran sudo systemctl enable ssh --now to enable ssh to begin the connection. Thereafter I ran, sudo systemctl status ssh to verify that ssh was enabled to allow connection from my virtual machine to the host device. By seeing that the Active status is shown as active (running), I know that it is now enabled. 

Overall reflection

First thoughts about completing this lab? It was generally straight forward and simple to complete. The learning curve for this was sufficient to get a clear understanding of what each step was for. 

In testing and development, this exercise has shown me that virtual machines are a better option that having physical devices to do the same job. Virtual machines provides flexibility, scalability, and security for the user who needs to know what are some potential consequences of each action carried out and how certain commands might affect how the system runs. It also gives the user a good gauge if the hardware configured is sufficient for their development and testing. 

During installation, I found that the resources to download were readily available. This means that in order to replicate the issue in another device is easier and hence it makes troubleshooting easier. Network setup was straight forward too. If there was a roadblock present, solutions can be sought from online communities easily and it is evident that the community is very willing to lend a helping hand to help the user maneuver their way out of an issue. 

Between a NAT and bridged networking, a NAT will allow the virtual machine to act as if it is the host device and allow it to access external resources. However, in a bridged network, this means that the virtual machine will receive its own IP address as if it is another device on the network. 
