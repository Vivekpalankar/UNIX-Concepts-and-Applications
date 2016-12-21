## Flex Your Brain

01. Display from /etc/passwd a list of users and their shells for those using the Korn shell or Bash. Order the output by the absolute pathname of the shell used.

    


02. Find out the next available UID in /etc/passwd after ignoring all system users placed at the beginning and up to the occurrence of the user nobody.

    


03. The **tar** command on one system can't accept absolute pathnames longer than 100 characters. How can you generate a list of such files?

    


04. Devise a sequence to examine recursively all ordinary files in the current directory and display their total space usage. Hard-linked files will be counted only once.

    


05. Invert the name of the individual in emp.lst (12.1) so that the last name occurs first.

    


06. Devise a shell script that kills a process by specifying its name rather than the PID.

    


07. From a **tar** archive print only the pathnames of directories. Directory pathnames end with a / but the **tar** output may contain a variable number of fields.

    


08. How do you list the users currently using the system along with a count of the number of times they have logged in?

    


09. Develop an **awk** program to summarize from the list of all processes, a count of processes run by every user (including root).

    


10. Write an **awk** sequence in a shell script which accepts input from the standard input. The program should print the total of any column specified as script argument. For instance, prog1 | awK_prog 3 should print the total of the third column in the output of prog1.

    


11. A stamp dealer maintains a price list that displays the country, the Scott catalog number, year of issue, description and price:  

        Kenya 288-92 1984 Heron Plover Thrush Gonolek Apalis $6.60
        Surinam 643-54 1983 Butterflies $7.50
        Seychelles 831-34 2002 WWF Frogs set of 4 $1.40
        Togo 1722-25 1996 Cheetah, Zebra, Anteloper $5.70

    Write an **awk** program to print a formatted report of the data as well as the total price. Note that the description contains a variable number of words.

    


12. Develop a control-break **awk** program that reads empn.lst and prints a report that groups employees pf the same department. For each department, the report should print  

    (i) the department name at the top.
    (ii) the remaining details of every person in the department.
    (iii) total salary bill for that department.

    Do you need to process the input before it is read by **awk**?

    
