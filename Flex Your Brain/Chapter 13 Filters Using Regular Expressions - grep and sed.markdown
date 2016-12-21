## Flex Your Brain

01. What is the difference between a wild-card and a regular expression?

    


02. Explain the significance of the * in this command: **grep 'botswana.\*birds' *.htm\***.

    


03. How will you list the ordinary files in your current directory that are not user-writable?

    


04. How many lines does **grep '.\*' foo** display? What happens if you remove the quote?

    


05. What is the significance of this command? **grep -l "`echo '\t'`" foo**

    


06. Use command substitution with **grep** to list the names of the persons from emp.lst who were born today.

    


07. How do these expressions differ? (i) [0-9]* and [0-9][0-9]* (ii) ^[^^] and ^^^

    


08. Are the following commands equivalent? **grep "^[^a-z]" foo** and **grep -v "^[a-z]" foo**

    


09. Frame regular expressions to match these patterns: (i) jefferies jeffery jeffreys (ii) hitchen hitchin hitching (iii) Heard herd Hird (iv) dix dick dicks dickson dixon (v) Mcgee mcghee magee

    


10. How will you remove blank lines from a file using (i) **grep**, (ii) **sed**? (A blank line may contain either nothing or only whitespace characters.)

    


11. How do you locate lines containing only printf but not fprintf using (i) **grep** (ii) **sed**? (Note that printf can also occur at the beginning of a line.)

    


12. How do you locate all non-blank lines that don't begin with #, /* or //?

    


13. Locate lines longer than 100 and smaller than 150 characters using (i) **grep**, (ii) **sed**.

    


14. Find out the occurrences of three consecutive and identical word characters (like aaa or bbb) using (i) **grep**, (ii) **sed**.

    


15. Devise a sequence to locate those users who have logged in yesterday or earlier but have not logged out, and mail the list to root. Users logged in more than once should feature only once in the list.

    


16. **grep -c ENCRYPTION foo** outputs the number of lines containing ENCRYPTION, but if the pattern sometimes occurs more than once in a line, how do you then obtain a count of all these occurrences? (HINT: Use **sed** also.)

    


17. Frame a command sequence that looks at romeo's mailbox to tell him that either he has received a message from henry or the Subject: line contains the word urgent or immediate in lower or uppercase.

    


18. Using **sed**, how do you add the tags <HTML> at the beginning and </HTML> at the end of a file?

    


19. How do you delete all leading and trailing spaces in all lines of a file?

    


20. How do you locate lines beginning and ending with a dot using (i) **grep**, (ii) **sed**

    


21. Explain what these commands do and if there's anything wrong with them:  

    (i) **sed -e 's/print/printf/g' -e 's/printf/print/g' foo**
    (ii) **sed -e 's/compute/calculate/g' -e 's/computer/host/g' foo


22. Every <B> tag in an HTML file has a closing </B> tag as well. Convert them to <STRONG> and </STRONG>, respectively, using **sed** with a single **s** command.

    


23. Specify the command sequence needed to remove the directory /usr/local/bin from the PATH defined in $HOME/.profile.

    
