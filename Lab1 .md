# Lab 1a Virtualisation and Linux Setup

Session 1a-1: Setting up Ubuntu and Linux on VMware Fusion

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

<img width="858" height="471" alt="Image" src="https://github.com/user-attachments/assets/a94b48eb-faf2-4ce1-a648-841283878bc3" />

Without opening the browser, I was able to check on my virtual machine's connectivity to the Internet by running ping -c 4 google.com. By indicating 4 within this line of code, it would only ping to the destination (google.com) 4 times. If there was no command of how many times ping should be carried out, it would continue endlessly. 

<img width="858" height="471" alt="Image" src="https://github.com/user-attachments/assets/582a7c94-d33f-46bd-afde-9277a5ef288d" />

Next I updated and upgraded ssh to ensure that I could remotely connect to another computer or cloud server securely over an unsecured network should it ever be used. 

<img width="858" height="471" alt="Image" src="https://github.com/user-attachments/assets/0ac03858-dbae-46fd-aa90-1102d797d1c2" />

In the screenshot above, I ran sudo systemctl enable ssh --now to enable ssh to begin the connection. Thereafter I ran, sudo systemctl status ssh to verify that ssh was enabled to allow connection from my virtual machine to the host device. By seeing that the Active status is shown as active (running), I know that it is now enabled. 

#Lab 1a-2: Ubuntu Desktop CLI Familiatisation 

In order to have a application for writing, LibreOffice is selected to be the application of choice. The package was downloaded from the official LibreOffice page. The files were extracted and installed based on the steps provided in their wiki page. sudo apt install libreoffice-writer -y was the code use to install LibreOffice Writer with it's essential core packages. Upon successful installation of Writer, it can be opened with the command libreoffice --writer. This will pull up the application as such: 

<img width="1210" height="708" alt="Image" src="https://github.com/user-attachments/assets/45a84f55-4e73-4286-9af2-c50b64c36522" />

<img width="525" height="753" alt="Image" src="https://github.com/user-attachments/assets/588e70e1-9bec-438b-8d63-8953cb27d422" />

At this point, to check all the current running processes, I entered ps -e to derive the above screenshot. 

<img width="525" height="753" alt="Image" src="https://github.com/user-attachments/assets/66259c14-62a2-41e3-8794-8c8aa99340ee" />

Next, I ran the command top to see what are the processes running in real-time. When I pressed 1, I noticed that there was another line of CPU showing up. This allows me to effectively monitor the resource usage on my system and give me a one glance to see if more resources are required to be catered for my use. To exit from this view, I hit q to end the monitoring session. 

<img width="525" height="753" alt="Image" src="https://github.com/user-attachments/assets/ca2dfa88-d0a4-40c3-8ba6-a2e288636092" />

<img width="525" height="753" alt="Image" src="https://github.com/user-attachments/assets/a4e2917d-2c6b-4b8f-b1f3-cad1770f2c4d" />

Next, I wanted to explore deeper into what my file system has. With ls, it lists all the files within the present working directory. By adding a -la, I am now able to see the permissions given for each file, the date of each file creation, file size, and the user  and group owner of each file. 

<img width="532" height="522" alt="Image" src="https://github.com/user-attachments/assets/73ca44cc-c6e8-47d8-ba1f-d474d33fd176" />

Lastly, I used ls -lah. this changed the way the file size was displayed as it was more human-readable now in the form of (Kb/Mb/GB).

<img width="940" height="267" alt="Image" src="https://github.com/user-attachments/assets/330ee0f2-cad1-4440-9742-8a5bef1e097a" />

I tried to create a new document called 'testfile' using the command touch testfile. As seen on the right side of the screenshot, it instantly created a file called testfile within the location I was currently on.

<img width="940" height="579" alt="Image" src="https://github.com/user-attachments/assets/b798a03f-db2b-45fc-91d4-1b9ee0596a41" />

To edit testfile, I tried to run gedit testfile. However, gedit was not installed in my terminal. So I ran the command sudo apt install gedit -y. After the installation was completed, I was able to open testfile. Using an alternate method to open testfile on terminal instead of UI, nano testfile was used. 

<img width="940" height="213" alt="Image" src="https://github.com/user-attachments/assets/68337292-51d3-409b-b857-01b3a29dde2e" />

From this screenshot, you can see that the file is open in both Terminal as well as in UI mode. Both methods are able to amend the same file. In order to exit from nano mode, I used command+X (mac user). One thing that I would like to point out is that, given a user was only granted access to Terminal and not the UI mode, gedit would not be possible in this case as it requires the UI to open the file. This makes nano a more diverse option for users to be able to amend the file whenever Terminal is accessible to them. 

Sometimes, when we would like to view a file rather than making any changes to it, cat is a command line that can be used in such situations. 

<img width="415" height="90" alt="Image" src="https://github.com/user-attachments/assets/0a395b8a-d8b2-463b-9ea5-33c246ec98a0" />

Alternatively, while less testfile is also a viable option to use to view the file, it provides a completely different perspective of how one views a file. You can quit from the view by pressing q. 

<img width="415" height="579" alt="Image" src="https://github.com/user-attachments/assets/aae1e409-07a2-4fff-ab59-a4e22984eb37" />

To make a quick copy of a file, cp testfile testfile2 was used in this instance. This created an exact copy of testfile and named it testfile2. 

<img width="415" height="198" alt="Image" src="https://github.com/user-attachments/assets/1bded833-a237-474d-8084-a3e538b39d3b" />

By running the code mv testfile2 testfile3, it renamed the file from testfile2 to testfile3. At this point, the content within testfile3 remains the same. 

<img width="424" height="451" alt="Image" src="https://github.com/user-attachments/assets/58c42950-bf32-4f4d-ad36-d5fc22f759c0" />

In the screenshot above, three commands were ran:

1. uname -a: Information was printed in a single line displaying which kernel version the VM is running on

2. lsb-release -a: Shows the current Linux Standard Base which contains the distribution and version number.

3. hostnamectl: Hostname information with a summary of the operating system within the VM is used.

<img width="415" height="403" alt="Image" src="https://github.com/user-attachments/assets/b0e32b79-c3c1-4f90-aaed-4de67ec92f55" />

ls -alt shows a different view where the files are now sorted from the most recently created file in a descending order. 

<img width="532" height="566" alt="Image" src="https://github.com/user-attachments/assets/d73d2735-04da-44a7-b7dc-bb5aa127bf09" />

whoami shows me the current user at the moment, which is lisa. However, without sudo, I was unable to add the user named student. By using sudo adduser student, I was able to add the user named student. I was also prompted to create a password of at least 8 characters with a complexity of lower and uppercase letters, number and special character. I could also change my user from lisa to root simply by entering sudo whoami. 

<img width="532" height="62" alt="Image" src="https://github.com/user-attachments/assets/d8e054a6-9c31-4d72-a0f7-2c2c8bdfdefc" />

<img width="858" height="471" alt="Image" src="https://github.com/user-attachments/assets/9066fecb-2ec7-4bcd-8785-ad2794083c14" />

Using ip a, I was able to have a glance of my current network configuration. 

<img width="858" height="471" alt="Image" src="https://github.com/user-attachments/assets/9066fecb-2ec7-4bcd-8785-ad2794083c14" />

Using ip a, I was able to have a glance of my current network configuration. 

<img width="532" height="224" alt="Image" src="https://github.com/user-attachments/assets/fe01c66f-847f-4ef4-bc48-ad3cfc8415a3" />

I was able to ping 8.8.8.8. 

















Overall reflection

First thoughts about completing this lab? It was generally straight forward and simple to complete. The learning curve for this was sufficient to get a clear understanding of what each step was for. 

In testing and development, this exercise has shown me that virtual machines are a better option that having physical devices to do the same job. Virtual machines provides flexibility, scalability, and security for the user who needs to know what are some potential consequences of each action carried out and how certain commands might affect how the system runs. It also gives the user a good gauge if the hardware configured is sufficient for their development and testing. 

During installation, I found that the resources to download were readily available. This means that in order to replicate the issue in another device is easier and hence it makes troubleshooting easier. Network setup was straight forward too. If there was a roadblock present, solutions can be sought from online communities easily and it is evident that the community is very willing to lend a helping hand to help the user maneuver their way out of an issue. 

Between a NAT and bridged networking, a NAT will allow the virtual machine to act as if it is the host device and allow it to access external resources. However, in a bridged network, this means that the virtual machine will receive its own IP address as if it is another device on the network. 
