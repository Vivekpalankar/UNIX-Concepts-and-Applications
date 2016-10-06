## Flex Your Brain

01. How will you obtain a complete listing of all files and directories in the whole system and save the output in a file?

    By running the command: `ls -lR / > listing.txt`. Root privilege may be required to run the command as many system direcotires are accessible to ordinary users.


02. Explain briefly the significance of the first four fields of the **ls -l** output. Who can change these attributes? Is there any attribute that can be changed only by the superuser?

    The first column shows the file type and the associated permissions for file owner, group owners and others.

    The second column indicates the number of links associated with the file.

    The third column shows the username of the file owner.

    The fourth column shows the group owner of the file.

    These attributes can be changed by the owner of the file as well as the system administrator. (Depending on the release of UNIX i.e. AT&T or BSD. See answer 12 below).

    Only system administrator can change the group ownership of a file to a group to which the owner doesn't belong.


03. Explain the significance of the following commands: (i) **ls -ld .** (ii) **ls -l ..**

    (i) **ls -ld .**: This command shows the attributes of the current directory in long listing format.

    (ii) **ls -l ..**: This command will list the contents of the parent directory in long listing format.


04. The commands **ls bar** and **ls -d bar** display the same output - the string bar. This can happen in two ways. Explain.

    If **bar** is an ordinary file, both the commands display **bar** as the output.

    If **bar** is a direcotry that contains only a single file or directory also named bar, than both the commands display **bar** as the output.


05. Does the owner always belong to the same group as the group owner of a file?

    Yes. But the group many not be the users primary group.


06. Create a file foo. How do you assign all permissions to the owner and remove all permissions from others using (i) relative assignment, (ii) absolute assignment? Do you need to make any assumptions about foo's default permissions?

    (i) `chmod u+rwx,o-rwx foo`

    (ii) `chmod 740 foo`

    In case of absolute assignment, we need to know the default permissions for the file foo to preserve the group permissions.


07. You tried to copy a file foo from another user's directory, but you got the error message cannot create file foo. You have write permission in your own directory. What could be the reason and how do you copy the file?

    The read permission may not be available for the source file. To copy the file, the appropriate read permission is required which can be set by either the file owner or the administrator.


08. Explain the consequences, from the security viewpoint, of a file having the permissions (i) 000 (ii) 777. Assume that the directory has write permission.

    (i) No one, including the owner of the file can do anything with the file. The file is technically unusable.

    (ii) Anyone can read, write or execute the file. The file is publicly accessible.


09. Examine the output of the two commands on a BSD-based system. Explain whether kumar can (i) edit, (ii) delete, (iii) change permissions, (iv) change ownership of foo:

    **$ who am i ; ls -l foo**  
    kumar  
    -r--rw----      1   sumit   kumar           78  Jan 27 16:57    foo

    There can be two course of actions depending on whether the user kumar belongs to the group named kumar. Both the cases are discussed one by one:

    Considering that user kumar also belongs to the group kumar:

    (i) kumar can edit the file as the group owners have write permission available.

    (ii) Whether kumar can delete the file will depend on user and group ownership and permission set for the directory housing the file foo.

    (iii) kumar cannot change the permissions of the file foo as he is not the owner of the file.

    (iv) kumar cannot change the ownership of the file foo as he is not the owner of the file.

    Considering that user kumar doesn't belong to the group kumar:

    (i) kumar cannot edit the file as the others do not have write permission available.

    (ii) Whether kumar can delete the file will depend on user and group ownership and permission set for the directory housing the file foo.

    (iii) kumar cannot change the permissions of the file foo as he is not the owner of the file.

    (iv) kumar cannot change the ownership of the file foo as he is not the owner of the file.


10. Assuming that a file's current permissions are rw-r-xr--, specify the **chmod** expression required to change them to (i) rwxrwxrwx, (ii) r--r----- (iii) --r--r-- (iv) --------, using both relative and absolute methods of assigning permissions.

    Assume that the file is named foo.

    Using relative assignemnt:

    (i) `chmod a+rwx foo`

    (ii) `chmod a-wx,o-r foo`

    (iii) `chmod a-wx,u-r foo`

    (iv) `chmod a-rwx foo`

    Using absolute assignment:

    (i) `chmod 777 foo`

    (ii) `chmod 440 foo`

    (iii) `chmod 044 foo`

    (iv) `chmod 000 foo`


11. Use **chmod -w .** and then try to create and remove a file in the current directory. Can you do that? Is the command the same as **chmod a-w foo**?

    No.

    Yes.


12. How will you determine whether your system uses the BSD or AT&T version of **chown** and **chgrp**?

    On an AT&T system, owner can change the owner and the group of a file. On a BSD system, owner of a file can be changed only by the superuser and the user can change the group of a file only to a group to which he or she already belongs.
