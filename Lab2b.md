## Lab 2b 

<img width="1702" height="657" alt="image" src="https://github.com/user-attachments/assets/3e64c57a-47a8-497f-8d38-2e071b93c9e2" />

Creating a new instance on AWS EC2 instance. 

<img width="1702" height="657" alt="image" src="https://github.com/user-attachments/assets/401a9af1-ed53-4e52-a6ae-0a0da022c951" />

Ensuring that rules allow for inbound connection to the internet. 

<img width="1702" height="525" alt="image" src="https://github.com/user-attachments/assets/55ffcf98-e60e-4218-a25b-3aa0fa304fca" />

Successfully downloaded the external file (EECS-2009-28.pdf) onto Ubuntu

<img width="1017" height="229" alt="image" src="https://github.com/user-attachments/assets/3e05fb69-e6f8-4bdf-ba35-47eea798801f" />

<img width="1703" height="1030" alt="image" src="https://github.com/user-attachments/assets/e5361766-9aed-4993-81f0-d7fa59212ffe" />

Link added to /var/www/html/index.html and updated to show the downloaded paper after clicking on the link. 

<img width="915" height="614" alt="image" src="https://github.com/user-attachments/assets/584914ac-ac47-4531-9b8d-9bff0970e918" />

Successful connection via SSH from virtual machine to EC2 instance. 

<img width="1714" height="215" alt="image" src="https://github.com/user-attachments/assets/50d134ea-ae0e-4636-94b0-0bad3de47618" />

Instance has been stopped upon completion of lab.


## Bash Coding

<img width="727" height="350" alt="image" src="https://github.com/user-attachments/assets/652c41fe-5cf9-43f1-9203-b4da8d6ddc83" />

mkdir was used to create a folder called Labfiles. touch was used to create the text file (notes.txt). cat opens the the text file and displays it without leaving the current terminal page. cp was used to make a copy of notes.txt and replicated to a new file called backup_notes.txt. mv was the command used to rename backup_notes.txt to old_notes.txt. rm was used to remove old_notes.txt.

<img width="495" height="180" alt="image" src="https://github.com/user-attachments/assets/bb1c09de-b9a5-4c65-8a9e-565d4d395e11" />

If chmod +x was given, it would have presented the user to be able to execute the file. The shebang used at the beginning of the script is meant to be an indication to the computer that this is now written as a script and should be run as a script as well. To personalise the experience when running a script, USER=$(whoami) can be added to the script to introduce a more personalised welcome message when a user runs the script. 

<img width="662" height="386" alt="image" src="https://github.com/user-attachments/assets/e862a5f4-1c32-498a-82c5-be59f3de682c" />

Script works as intended. for loop in this case works like a counter, whenever the script is ran, the counter starts from 1 and counts to 5 every 1 second. In the event where a user enters a number greater than 10, it will show that the number is out of range. 

<img width="405" height="208" alt="image" src="https://github.com/user-attachments/assets/50dae1e8-f235-4ac2-a087-577af11d5869" />

<img width="666" height="306" alt="image" src="https://github.com/user-attachments/assets/48c9469c-2ee4-4084-b7fd-027680c08d7e" />

Successful run of resource_monitor.sh. free -h provides infromation of the memory used by system and how much free space is left. In order to include network usage, the script can be modified by adding the df command to the bash script. 
