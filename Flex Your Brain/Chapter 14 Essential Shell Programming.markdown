## Flex Your Brain

01. Devise a script that takes a filename as argument (which must exist in the current directory) and locates from your home directory tree all pathnames of its links. The list should be mailed to self.

    


02. Use a script to take two numbers as arguments and output their sum using (i) **bc**, (ii) **expr**. Include error-checking to test whether two arguments were entered. Should you use **bc** or **expr** for computations?

    


03. Write a script that lists files by modification time when called with **lm** and by access time when called with **la**. By default, the script should show the listing of all files in the current directory.

    


04. Expand the scope of the script in 14.13 (Test Your Understanding) to perform the search recursively.

    


05. Write a script that behaves both in interactive and non-interactive mode. When no arguments are supplied, it picks up each C program from the current directory and lists the first 10 lines. It then prompts for deletion of the file. If the user supplies arguments with the script, then it works on those files only.

    


06. Display the processes in system every 30 seconds five times using a (i) **while** loop, (ii) **for** loop. What is the unusual feature of the **for** loop?

    


07. You are moving files to a hand-held which accepts only 8+3 type filenames. Produce a list of those files in your current directory that fail in this test.

    


08. Write a script that displays a special formatted listing showing the (i) permissions, (ii) size, (iii) filename, (iv) last modification time, (v) last access time of filenames supplied as arguments. Provide suitable headers using the **printf** command.

    


09. Find out the pathname of the Korn shell on your machine and then change the interpreter line in all shell scripts in the current directory that shows a different pathname for **ksh**.

    


10. Observe this command; does it make any sense? **set `set`**.

    


11. Write a script which looks up every .c file in the current directory for the strings printf or fprintf. If found, the script adds the statement `#include <stdio.h>` at the beginning of the file but only if it doesn't already have it included.

    


12. Write a script that compares two directories bar1 and bar2 (supplied as arguments) and copies or overwrites to bar1 from bar2 every file that is either not present in bar1 or is newer than its namesake in bar1. (HINT: Use the **find** command).

    


13. You have a number of C programs that contain comment lines at the beginning of each program. The lines begin with /* followed by the first line of comment, but the terminator line has */ as the only character in the line. Remove these comments from all files.

    


14. Write a script that monitors the creation of .pdf or .PDF files in the current directory. Every minute is should display a list of those filenames created after the previous display.

    


15. Write a shell script that uses **find** to look for a file and echo a suitable message if the file is not found. You must not store the **find** output in a file.

    


16. Write a script that checks each minute and reports on who logs in who logs out.

    


17. Assume that you have a number of files, downloaded from the Internet, in the /home/kumar/download directory. The table of contents (TOC) is available in the file TOC_download.txt in the form _filename:description_. The script should check each file in the download directory that doesn't have a description in the TOC file and prompt the user for the description . The TOC should be updated to maintain the list in sorted condition. The script must be immune to signals.

    
