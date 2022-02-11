### Artifact 1
- Website defacement (index.htm)
_______________________________________
1. Performed nmap scan of bullfrog and saved results onto a file called bullfrog_nmap
	- nmap -sC -sV -p- 30 192.168.220.32 -oN bullfrog_nmap  
2. Saw telnet opened and attempted to connect using given Credentials
	- ![[Pasted image 20220210204536.png]]
	- After several tries, the credentials were Administrator:St0lentTruck!
3. Once logged on, I tried several commands that did not work (ls, dir), but noticed it said you have mail
	- I typed mail and it brought me to an email message
![[Pasted image 20220210204749.png]]

4. Saw pwd=/home/administrator, so continued on that venue
	- Performed cd .. to go back one directory and found many other users
![[Pasted image 20220210205041.png]]
	- There was nothing in the directories
5. Went to /var/www to access web server files
![[Pasted image 20220211123759.png]]
6. Accessed index.htm (default site) and performed a web defacing attack
	- sudo nano index.html
	- ![[Pasted image 20220211124909.png]]

### Artifact 2
- Breach note
_______________________________________
7. Used dirbuster to brute force directories and file names on web server.
	- ![[Pasted image 20220211125946.png]]
	- Found an interesting directory called tftproot
	- ![[Pasted image 20220211130651.png]]
	- We were able to access it through our Kali Linux browser
	- ![[Pasted image 20220211130744.png]]
- Obfuscated tftproot directory by using mv tftproot .tftproot
- Created many layers of directories and left a note on the deepest layer
- ![[Pasted image 20220211132751.png]]
- Timestamp on my system
- ![[Pasted image 20220211131511.png]]

### End Results
_______________________________________
![[Pasted image 20220211132844.png]]

![[Pasted image 20220211132920.png]]