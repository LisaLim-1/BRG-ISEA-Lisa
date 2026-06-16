#Lab 1b Linux Services, SSH, Firewalls & Compression


<img width="645" height="540" alt="Image" src="https://github.com/user-attachments/assets/291e1daf-a237-442c-8f3b-b2da10b17985" />

Installing apache2 and nmap using Terminal

<img width="680" height="731" alt="Image" src="https://github.com/user-attachments/assets/bd69e1e7-db75-4453-97b2-8348cde935d1" />

Reflects Apache welcome page on http://127.0.0.1.

<img width="609" height="222" alt="Image" src="https://github.com/user-attachments/assets/ee84bc12-ed05-4b5b-bc52-3b321e112d60" />

By running nmap, it shows that there are currently 3 ports open. 

<img width="682" height="604" alt="Image" src="https://github.com/user-attachments/assets/516ebad7-25f8-4ab2-85be-a3eee7a71e37" />

<img width="647" height="529" alt="Image" src="https://github.com/user-attachments/assets/f6e4a31b-8dc0-4539-887d-b10d13494bd2" />

Apache2 was uninstalled which cause the page to fail from loading and when nmap was run, there is one less port open (port 80). 

<img width="645" height="493" alt="Image" src="https://github.com/user-attachments/assets/b646a498-f3c7-4089-810a-ae4193407bdd" />

Port 80 is now enabled 

<img width="651" height="745" alt="Image" src="https://github.com/user-attachments/assets/fd982c50-d2a4-4716-8bf3-1a664d7aceeb" />

SSH is running and able to connect to localhost

<img width="651" height="338" alt="Image" src="https://github.com/user-attachments/assets/85f26e3d-8c68-45b5-bac6-118890722da1" />
<img width="651" height="43" alt="Image" src="https://github.com/user-attachments/assets/5e160436-3706-434b-b7d1-0bd2b2756b25" />

Adding a new user called Emily Porkshop, user account is now found in less /etc/passwd

<img width="651" height="388" alt="Image" src="https://github.com/user-attachments/assets/ba56f7a0-6590-49ed-94f8-5a3a3729aee8" />

User Emily is able to access my localhost. 

<img width="637" height="557" alt="Image" src="https://github.com/user-attachments/assets/ca691763-4677-4812-af44-b89b028d259e" />

Downloaded books from gutenberg using wget. Port 443 was not opened, so opened on ufw using sudo ufw allow 443/tcp
and managed to download the files. Files were moved from Downloads folder into books folder. The files were then subsequently zipped. However when comparing file sizes, books file size was 4096 bits whereas books.tar.bz2 came in at 316156 bits. Upon reading deeper, it was learned that books file was treated like index of a bigger file, meaning it would only consume the default block size of 4096 bits. However since books.tar.gz is a compressed file of the different books within it, the file size reflects as such instead. 

<img width="1279" height="166" alt="Image" src="https://github.com/user-attachments/assets/e6c712e5-67f6-48dc-939e-3f73f89a36d2" />

scp moving file from /home/lisa to /home/lisa/Downloads/.

<img width="1204" height="385" alt="Image" src="https://github.com/user-attachments/assets/dcdc1f52-c706-4e8b-a4d9-d802c603a10d" />

ssh into another account and created a test folder

<img width="726" height="92" alt="Image" src="https://github.com/user-attachments/assets/63112006-e39f-4169-a6db-ccef9869d65b" />

Upon creation of the folder, a text file was created (helloEmily.txt). Subsequently, the file was updated with a greeting using echo into helloEmily.txt. 

<img width="726" height="54" alt="Image" src="https://github.com/user-attachments/assets/02a21c32-03bb-4177-85b7-9ed8787d41a7" /> 

While in the ssh session as emily, I was unable to run the gedit command. This is due to the rights given to emily. As a user of this system, she was only entitled to read rights.

<img width="538" height="669" alt="Image" src="https://github.com/user-attachments/assets/3b785f79-a79f-442f-87ea-e76f3dca2a32" />

<img width="627" height="56" alt="Image" src="https://github.com/user-attachments/assets/5374f891-f636-44cd-b7ae-9f88487f3b80" />

Creating users alice, bob and mallory. Create group sharedgroup as well. 

<img width="538" height="38" alt="Image" src="https://github.com/user-attachments/assets/557105de-30fc-4acd-bfcb-edf1de128ff9" />

<img width="627" height="74" alt="Image" src="https://github.com/user-attachments/assets/60de0b37-dc31-42bd-a59f-3636335de0ac" />

Added alice and bob to sharegroup

<img width="627" height="324" alt="Image" src="https://github.com/user-attachments/assets/2cf05889-6e0b-4f0a-85bb-1c5a28cfb3c1" />

shared directory is created in /home 

<img width="627" height="324" alt="Image" src="https://github.com/user-attachments/assets/a8c2bc0d-da36-4bfb-9619-aaa0c79b13c4" />

created 10 files in shared folder



Permission granted to owner (read, write, execute) and group (read and execute) but not to user.




