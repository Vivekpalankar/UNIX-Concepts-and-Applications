## Flex Your Brain

Incorporate error checking wherever possible and relevant. File I/O operations are to be performed using only the **read** and **write** system calls, and not library functions.

01. Explain what an atomic operation is. How do you open a file and (i) truncate it if it exists, (ii) create it if it doesn't? What is the advantage of using **open** to create a file instead of **creat** which is designed for only that purpose?

    


02. Write a program that copies a file and accepts the source and destination as its two arguments. The destination can also be a directory.

    


03. Modify the program in 23.9 (Test Your Understanding) so that it displays the output in lowercase when invoked by the name **lower** and uppercase when invoked by **upper**. What else do you need to do to run it?

    


04. Explain why the selection of the buffer size used by **read** and **write** is crucial in writing efficient programs.

    


05. Write two programs that read /etc/passwd using (i) a single-character buffer, (ii) a buffer of 2048 bytes with **read**. Use the **time** command with each and compare their performance.

    


06. Devise an advisory locking mechanism which allows two programs **lock1.c** and **lock2.c** to read a file foo only if the file .lockfile doesn't exist. Both programs will first create the file if it doesn't exist, and remove it before termination.

    


07. Write a program to split the contents of a file into multiple files so that each file contains at most 10,000 bytes. Name the files foo.1, foo.2 and so forth.

    


08. Write a program that uses complete error checking to perform the following on an existing file foo: (i) opens foo and then deletes it without closing it, (ii) reads foo and displays its output, (iii) opens foo again. After the program has completed execution, check whether foo has actually been deleted. Explain your observations and the behavior of the **unlink** system call.

    


09. Write a program that moves a group of files to a directory. The file names are provided as arguments and the last argument is a directory. Provide adequate checks to ensure that the file exists and have the expected file type. If the last argument doesn't exist , then create a directory by that name.

    


10. Write code to create a file foo1 with the same permissions, modification time and access time as another file foo2.

    
