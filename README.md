# Linux File Permissions Management

## Objective

This project demonstrates how to manage and correct file and directory permissions in a Linux environment. Using command line tools, I identified files with incorrect permissions, applied changes to secure access, and verified modifications for both regular and hidden files.

## Skills Learned

-Proficiency in Linux command line interface (CLI) for system administration tasks.

-Understanding of file and directory permission structures (r, w, x) and ownership (user, group, others).

-Ability to apply chmod to manage read, write, and execute permissions.

-Experience handling hidden files and directories.

-Verifying permission changes using ls -l and ls -la.

## Tools Used

-Linux terminal / CLI

-Commands: ls, ls -l, ls -la, chmod

-Hidden files and directories handling (. prefix)

# Steps

## 1. Check file and directory permissions
ls -la

<img width="957" height="233" alt="Screenshot 2025-08-19 105202" src="https://github.com/user-attachments/assets/84c3ecfc-ab72-44a6-806a-9d1233edc38d" />

Lists all files, including hidden files, with detailed permission strings.

## 2. Change file permissions for users and groups
chmod u+w,g-r project_x.txt

<img width="737" height="221" alt="Screenshot 2025-08-19 110339" src="https://github.com/user-attachments/assets/ac260bd3-c578-40ac-b88b-7f1be1626680" />

Adds write permission for the user (u+w) and removes read permission for the group (g-r).

chmod g-w,g+r .project_x.txt


Adjusts permissions on a hidden file (note the . prefix). Removes write access from the group and adds read access.

## 3. Change directory permissions
chmod g-x drafts
ls -l

<img width="668" height="167" alt="Screenshot 2025-08-19 111050" src="https://github.com/user-attachments/assets/6fafda9e-4c36-44d8-9a78-05c2b79009d9" />

Removed execute permission for the group on the drafts directory to restrict access. Verified changes with ls -l.

# Summary

In this project, I first reviewed file and directory permissions using ls -la to identify items with incorrect access. I then modified permissions using chmod to:

  -Remove unnecessary write access and add required read access for groups.

  -Handle hidden files correctly by including the . prefix.

  -Restrict directory access to the user by removing execute permission for the group.

This project demonstrates practical Linux system administration skills, particularly in managing user and group permissions to enhance file and directory security.
