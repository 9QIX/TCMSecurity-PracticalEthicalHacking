# Managing Users and Permissions in Linux

## File Permissions

- `ls -l` shows file permissions in the format: file type, owner permissions, group permissions, all user permissions
- Permissions are represented as r=read, w=write, x=execute
- chmod command changes file permissions
  - `chmod 777 file` gives full read/write/execute permissions
  - `chmod +x file` adds execute permission

## Users

- `adduser` command adds a new user
- `/etc/passwd` file lists all users
- `/etc/shadow` contains hashed passwords (crackable)

## Switching Users

- `su` switches to another user if you have their password
- `sudo` allows running commands as root or another user with permissions listed in `/etc/sudoers`

## User Privileges

- Root user has full system access
- New users have minimal permissions by default
- Users listed in `/etc/sudoers` can run commands with elevated privileges using `sudo`

This covers the basics of managing file permissions, creating users, switching between users, and understanding user privilege levels - all critical concepts for penetration testing and system security.
