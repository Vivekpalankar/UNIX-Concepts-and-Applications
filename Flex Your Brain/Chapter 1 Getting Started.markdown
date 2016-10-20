## Flex Your Brain

01. Operating systems like UNIX provide services both for programs and users. Explain.

    A computer hardware is a bare machine with no intelligence of its own. An operating system like UNIX is a special software which provides the computer with basic intelligence in the form of services.

    A few examples of services for programs include using the CPU, allocating memory, accessing devices like hard disk for reading and writing files.

    A few examples of services for users include file management (copying and deleting files, creating directories), determining other users working in the network, sending a mail message to a friend.


02. What does a program do when it needs to read a file?

    The program makes a call to the operating system using a specially designed interface (called **System Call**), which in turn performs the job and makes the data available to the program.


03. When you log in, a program starts executing at your terminal. What is this program known as? Name four types of this program that are available on a system.

    The program is referred to as the users Login shell. Some of the popular shell program generally available on a UNIX system are:

    -   sh (the primitive Bourne Shell)
    -   csh (C Shell)
    -   ksh (Korn shell)
    -   bash (an enhanced version of original Bourne shell)


04. What exactly happens when you enter this sequence: **ls > list**?

    The output of the **ls** command is saved in a file named _list_ in the current directory.

    The shell gets to see the redirection operator when interpreting the command line. It opens the file following the > operator (here, _list_). Next the command **ls** is run which reads the directory file corresponding to the current directory. The shell has manipulated things so that the output of the **ls** command doesn't go to the terminal but is written to the file opened by the shell on its behalf.

    _Note_:     The file is created anew if it doesn't already exist, or is overwritten with the command output if it does exist. An error occurs if either the named file exists and is not writable by the current user, or the named file doesn't exist and the directory is not writable by the user.


05. Attempt the variable assignment x=10 by providing a space on either end of the =. Why doesn't it work?

    The shell programming syntax states that there should be no spaces on either side of = operator.

    When entering `x =10`, _x_ is treated as a command by the shell. Since there is no command (internal or external) named _x_, the shell shows an appropriate error message stating that the command doesn't exist.

    Similar error occurs in case `x= 10` is entered where _10_ is treated as a command, but the shell fails to locate it.


06. Run the following commands and then invoke **ls**. What do you conclude?  
    `echo > README[Enter]`  
    `echo > readme[Enter]`

    Two empty files named _README_ and _readme_ are created in the current directory.

    _Note_: When running on a case-insensitive file-system, only one file named _README_ is created. If either of the two files already exists, its content is overwritten with an empty file.


07. Enter the following commands and note your observations: (i) **who** and **tty** (ii) **ps** and **echo $$**

    1.  **who** command outputs a list of all users currently logged on, showing for each user the login name, tty name, the date and time of login, and host-name if not local.

        **tty** command outputs the absolute path of the device file corresponding to the terminal attached to the standard input/output.

    2.  **ps** command outputs a list of all the currently running processes corresponding to the logged in user.

        **echo $$** outputs the integer PID corresponding to the running shell process.


08. Name the three commands that you would try in sequence to log yourself out of the system. Which one among them will always work?

    `[Ctrl-d]`, `logout` and `exit`. `exit` command is guaranteed to always work.


09. What is the significance of your user-id? Where in the system is the name used?

    The user-id is used to uniquely identify a user in the operating system. user-id gets associated with any file or process created by the user.

    The name is used to identify the user with other users and for display in command outputs.


10. What is the one thing that is common to directories, devices, terminals and printers?

    They are all represented as files in the UNIX file-system.


11. Name some of the duties of the system administrator that you have encountered so far.

    Backing up files. Restoring a system to a usable state in case a crash occurs. Startup, shutdown and maintenance of the system. Administering the system. Creating and administering user accounts. Updating system date.

12. What are the two schools of UNIX that initially guided its development?

    AT&T and The University of California, Berkeley (UCB).
