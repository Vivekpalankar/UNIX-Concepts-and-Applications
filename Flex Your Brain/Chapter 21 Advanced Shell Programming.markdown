## Flex Your Brain

01. Write a script which accepts an anonymous FTP site (like ftp.heavens.com) and any number of **ftp** commands (like **"cd pub", "get cp32.tar.gz"**) as arguments. It should then connect to the site, log in automatically, and execute the **ftp** commands.

    


02. Why won't the **exit** command, when placed in a shell script like this, terminate the script? How do you get over this? **(** statements **exit )**

    


03. Invoke the **su** command (if you know the root password), and then run **ps -t** with the terminal name. What conclusion would you draw?

    


04. Write a shell function that locates a directory supplied as argument, in the home directory tree and switches to it. Will the same code work if placed in a shell script?

    


05. What is wrong with this statement? How do you modify it to execute correctly?  

        **[ $# -ne 2] && echo "Usage: $0 min_guid max_guid" ; exit**

    


06. You have to run a job at night and need to have both the output and error messages in the same file. How will you run the script?

    


07. How can you extract the last command line argument to a script using (i) arrays, (ii) **eval**?

    


08. Write a script to copy files to a directory only when they don't exist there. The filenames are supplied as arguments and the last argument is the directory. You are allowed to use only one  external command (**cp**) and exploit the features of the Korn and Bash shells. (HINT: Use the **eval** statement to identify the directory name.)

    
