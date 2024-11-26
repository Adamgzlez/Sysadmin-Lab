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


4. Create New User Accounts
5. Create New User Group and Collaboratived Folder\
6. Installing and Using Lynis Audit
7. Installing and Using Chrootkit
