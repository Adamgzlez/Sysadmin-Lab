# Sysadmin Lab

## Objective

The Sysadmin Lab is aimed to establish a new server to replace a malfunctioning Linux server. The primary focus was to check user permissions on sensitive files, create user accounts, create a user group and collaborative folder, using lynis to audit the new server, and install chkrootkit to search for any potential rootkits that may have been installed. This hands-on experience was designed to deepen understanding of network security, creating and modifying a new server, and defensive strategies.

### Skills Learned

- Create and assign users for services.
- Auditing the services being ran on the server.
- Analyzing permissions on sensitive files and changing permission if needed.
- Making group folders and assigning users

### Tools Used

- Local virtual machine.
- Lynis package.
- chkrootkit package.
- Virtual box/Ubuntu VM.

## Steps

1. Ensuring Permissions on Sensitive Files

Inspecting and analyzing permissions on files to allow read, write, and allow everyone read access

Commands to inspect permissions
```
ls -l /etc/shadow
```
```
ls -l /etc/gshadow
```
```
ls -l /etc/group
```
```
ls -l /etc/passwd
```
2. Setting Permissions on Sensitive Files
```
sudo chmod 600 /etc/shadow
```
```
sudo chmod 600 /etc/gshadow
```
```
sudo chmod 644 /etc/group
```
```
sudo chomod 644 /etc/passwd
```
3. Create New User Accounts
Commands adding new users and assigning admin to the sudo group.
```
sudo useradd sam, sudo useradd joe, sudo useradd amy, sudo useradd sara, sudo useradd admin
```
3a. Adding admin to the sudo group.
```
sudo usermod -a -G sudo admin
```
4. Create New User Group and Collaboratived Folder
Commands adding a new group and adding users to it. Also creating a shared folder and changing ownership to that new group.
```
sudo groupadd engineers
```
```
sudo usermod -a -G engineers sam, sudo usermod -a -G engineers joe, sudo usermod -a -G engineers amy, sudo usermod -a -G engineers sara
```
```
sudo mkdir /home/engineers
```
```
sudo chown 0:1019 /home/engineers
```
5. Installing and Using Lynis Audit
Commands to install and run lynis on the system.
```
sudo apt install lynis
```
```
sudo lynis audit system
```
6. Installing and Using Chrootkit
Commands to install and run chrootkit expert mode on the system.
```
sudo apt install chkrootkit
```
```
sudo chkrootkit -x
```
