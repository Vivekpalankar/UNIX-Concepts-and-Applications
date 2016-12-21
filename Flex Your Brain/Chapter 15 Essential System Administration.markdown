## Flex Your Brain

01. Why is the **su** command terminated with **exit**? What is the difference between **su** and **su - romeo**?

    


02. Name five administrative functions that can't be performed by a non-privileged user.

    


03. If the administrator doesn't want romeo to user the **at** command but allows juliet to user **cron**, what does he need to do?

    


04. A program can be made to run with the privileges of its owner. Explain the feature that allows this and how you can use it make a program run with the privileges of root.

    


05. Explain what these commands do:  

    (i) **find / -perm -4000 -print**
    (ii) **find / -type d -perm -1000 -exec ls -ld {} \;**
    (iii) **find / -type f -size +2046 -mtime +365 -print**

    


06. How will you arrange for a group of users to write to the same directory and yet not be able to remove one another's file?

    


07. How will you create a user guru with UID 212 and GID dialout (a new group)? guru will use Bash as his shell and be placed in the /home directory. How can you later change guru's shell to Korn without editing /etc/passwd?

    


08. A user romeo belongs to the student group, and yet /etc/group doesn't show his name beside the group name. How can that happen?

    


09. How do you display the run level for your system? What is the difference between run levels 0 and 6?

    


10. Explain the difference between (i) block and character devices, (ii) major and minor numbers. Can two devices have the same major and minor numbers?

    


11. Write a shell script to copy a floppy diskette.

    


12. Specify the **tar** and **cpio** command lines that will (i) prevent files from being overwritten during restoration, (ii) rename each file interactively during restoration, (iii) append to an existing archive during copying.

    


13. The command tar **xvf /dev/fd0 *.c** displays an error message even though the diskette contains a number of .c files. Name two reasons that can make this happen.

    

