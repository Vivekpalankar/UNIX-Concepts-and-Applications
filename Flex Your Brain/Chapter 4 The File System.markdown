## Flex Your Brain

01. Name the two types of ordinary files and explain the difference between them. Provide three examples of each type of file.

    Ordinary files can be classified into two types: _text_ and _binary_. A text file contains only printable characters from the ASCII character set while a binary file generally contains characters from the entire spectrum of ASCII character set.

    C program source code, perl script file and ASCII text readme files are examples of text files.

    Compiled C executable, a PNG image file and a wav audio file are examples of binary files.


02. How does the device file help in accessing the device?

    A device file helps in accessing a device by making itself available for reading and writing via system calls and by setting appropriate file attributes.


03. Which of these commands will work? Explain with reasons: (i) **mkdir a/b/c** (ii) **mkdir a a/b** (iii) **rmdir a/b/c** (iv) **rmdir a a/b** (v) **mkdir /bin/foo**

    1.  **mkdir a/b/c**: Won't work. Directory **a** and **a/b** needs to exist before attempting to create **a/b/c**.

    2.  **mkdir a a/b**: Will work. Directory **a** will be created first followed by directory **a/b**.

    3.  **rmdir a/b/c**: Will work. Directory **c** exists and is empty, as evident from the last command.

    4.  **rmdir a a/b**: Will work partially. Directory **a** won't be removed as its non-empty. Directory **a/b** will be removed as its empty.

    5.  **mkdir /bin/foo**: Won't work. **/bin** is writable only by root user. To create a file or directory in /bin, either login as root user or use `sudo` command.


04. If **mkdir test** fails, what could be the possible reasons?

    Either **test** already exists as a file or directory in the current directory, or the user doesn't have write permission for the current directory.


05. Which of these files or directories can you create? Explain with reasons: `.`, `..`, `...` and `....`

    Only `...` and `....` can be created either as a file or a directory. `.` and `..` are special names reserved for use by UNIX to refer to the current and the parent directory.


06. The command **rmdir bar** fails with the message that the directory is not empty. On running **ls bar**, no files are displayed. Why did the **rmdir** command fail?

    The directory **bar** may contain hidden files and hence may not be empty. Alternatively, the user may not have write permission for the current directory.


07. Suppose you have to develop a script that refers to a file in charlie's home directory. How will you specify the location of this file in your script to make sure that it works even when charlie's home directory changes?

    By referring to charlie's home directory as `~charlie`.


08. Explain the difference between the commands **cd ~charlie** and **cd ~/charlie**. Is it possible for both commands to work?

    **cd ~charlie** changes the current working directory to charlie's home directory. **cd ~/charlie** attempts to change the current working directory to a directory named _charlie_ inside charlie's home directory. The latter command may fail if no such directory exists.


09. Why do we sometimes run a command like this - **./update.sh** instead of **update.sh**?

    To refer to the file present in the current directory and not some other file with the same name existing in a directory present in the users PATH.


10. What is the sort order prescribed by the ASCII collating sequence?

    Numbers followed by uppercase alphabets followed by lowercase alphabets.


11. Assuming that you are positioned in the directory /home/kumar, what are these commands presumed to do and explain whether they will work at all: (i) **cd ../..** (ii) **mkdir ../bin** (iii) **rmdir ..** (iv) **ls ..**

    1.  **cd ../..**: Change the current directory to the root directory `/`. It will work successfully if the user has execute permission available for the root directory.

    2.  **mkdir ../bin**: Create a directory named **bin** in **/home** directory. The command will fail if either the user doesn't have write permission available for **/home** or **/home/bin** already exists as a directory or file.

    3.  **rmdir ..**: Won't work. This command attempts to remove the parent directory i.e. **/home** while being placed in the child directory **/home/kumar**, which shell doesn't permit.

    4.  **ls ..**: This command will attempt to list the contents of the parent directory i.e. **/home**. Will succeed only if the user has read permission available for **/home**.
