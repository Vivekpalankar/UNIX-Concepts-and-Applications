## Flex Your Brain

01. How does an executable C program differ from its associated object files?

    


02. It makes no sense to save object files if other programs are not going to use them. Right or wrong?

    


03. Explain the significance of the -c, -o and -l options of the C compiler.

    


04. Modify the application presented in Section 22.2 to implement the following:  

    (i) The **compute** function should be in a separate file, **compute.c**, and its **include** statement in **compute.h**.
    (ii) All function prototypes should be defined in a single file, **prototype.h.

    Modify makefile2 discussed in Section 22.3.2 accordingly.

    


05. Look up the man page of **make** to find out how it can be invoked to display the command line that it would execute without actually executing it.

    


06. Explain how **make** may run without error with a makefile that contains only the following entry. What command will it run?  

        foo:

    


07. A **make** rule doesn't always have a dependency and the target need not be a disk file. Explain with an example of a makefile entry.

    


08. Specify the commands that will (i) create an archive named foobar.a containing the object files **foo1.o** and **foo2.o** from the archive. Can this archive be used with the -l option to **cc**?

    


09. What does this entry in a makefile mean? What command does **make** run if **a.h** if modified?  

        foo.a(a.o): a.h

    


10. SCCS and RCS basically use the same mechanism to store file versions except that they work in opposite directions. Explain. Which system do you think reconstructs a version faster?

    


11. You have three versions of a program  named **foo1.c**, **foo2.c** and **foo3.c**. Mention the steps needed to check in all three versions to a single SCCS file.

    


12. Mention the set of commands that produce the deltas 1.1, 1.2, 1.3 and 1.2.1.1 of **foo.c**. Now use **get -r9 s.foo.c** and **get -e -r9 s.foo.c**. What do you observe?

    


13. Which file does **sact** obtain activity information from? When it the file created and deleted?

    


14. You checked out a delta with **get -e s.foo.c**, and then realized that you shouldn't have done so. What should you do now and why?

    
