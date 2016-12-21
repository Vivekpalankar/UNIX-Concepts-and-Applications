## Flex Your Brain

01. Detect the errors in the following program (line numbers on left):  

        1       # foo.pl -- Checking file system block size
        2       #/usr/bin/perl
        3       print "Enter the block size of your file system: "
        4       bs = <STDIN> ;
        5       chop ($bs) ;
        6       if ( $bs > 8192 )
        7           print "Lot of wasted space /n" ;
        8       } else {
        9           print "Reasonable size" ;
        10      }

    


02. Write a one-liner to print double-spaced lines from a file.

    


03. Write a program to convert a binary number specified as argument to decimal. (HINT: Use the **reverse** function.)

    


04. Write a program that looks up /etc/passwd and /etc/groups and prints (i) the highest UID (ii) the login name, real name and GID (both number and name) of that user.

    


05. Devise a script which lists the usage of words (in the form word: count) in its argument files.

    


06. Write a program that populates an array named weekday from the string SunMonTueWedThuFriSat, and then prints each day in uppercase.

    


07. How will you use **find** and **perl** to delete all ordinary files modified more than a year back? What is the advantage of using this method compared to using **find** with -exec rm?

    


08. (i) Write a one-liner to change the interpreter line to #!/usr/local/bin/perl in all .pl files in the current directory. (ii) Enlarge the scope to add the interpreter line if it doesn't exist. Also, don't make any substitution if a proper interpreter line is already in place.

    


09. A closing HTML tag starts with /. For instance, <b> is closed with </b>. Convert all these tags comprising single words (without attributes) to uppercase. (Tags like <img src=... must not get converted.)

    


10. A file contains a set of numbers and strings as shown by these sample entries:  

        1
        5
        3
        botswana
        namibia
        swaziland

    Devise a _generalized_ program that prints 1. botswana on the first line, 5. namibia in the second line, and so forth. It does not matter how many sets of entries there are in the file, as long as the set of numbers is followed by an equal number of country names.

    


11. Refer to the stamp dealer problem in Exercise 18.11 and implement it in **perl**.

    
