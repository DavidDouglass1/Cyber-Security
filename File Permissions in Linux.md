# File permissions in Linux


## Project description

This project is a demonstration of Linux file and directory access, and identifying and changing file permissions.


## Check file and directory details

Checked the contents of /projects directoryusing ls -la after using cd command to navigate to the proper directory. 


## Describe the permissions string

The first digit describes if the object is a file or directory by denoting a “d” for directory and a - for file.  Digits 2-4 indicate the user’s (creator of the file) read, write and executable permissions of a file by a w, r, and e or a “-” if permission is denied.  Digits 5-7 indicate the permissions for the group.  Digits 8-10 indicate permissions for “other”. 


## Change file permissions

Using the “chmod o-w project_k.txt” command, all files that allow others write access have been changed to deny write access.


## Change file permissions on a hidden file

Using the “chmod u=r,g=r .project_x.txt” command, this hidden file was set to read only for the user and group.


## Change directory permissions

Using the “chmod g-x drafts” command, the drafts directory is now only accessible by the user, “researcher2”.


## Summary

This was a small exercise to verify that files and directories have the proper permissions.
