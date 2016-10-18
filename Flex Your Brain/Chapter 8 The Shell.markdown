## Flex Your Brain

01. When the shell finds metacharacters in the command line what does it do? When is the command finally executed?

    The shell performs all the actions represented by the metacharacters before executing the command line.

    After completing this pre-processing step (wild-card expantion, variable evaluation, command substitution, opening appropriate files, connecting streams) shell submits the command line to the kernel for final execution.


02. Devise wild-card patterns to match the following filenames: (i) foo1, foo2 and Foo5 (ii) quit.c, quit.o and quit.h (iii) watch.htm, watch.HTML and Watch.html (iv) all filenames that begin with a dot and end with .swp

    (i) [f]oo[12] and Foo5

    (ii) quit.[coh]

    (iii) watch.{htm, HTML} and Watch.html

    (iv) .*.swp


03. Devise wild-card patterns to match all filenames comprising at least three characters (i) where the first character is numeric and the last character is not alphabetic, (ii) not beginning with a dot, (iii) containing 2004 as an embedded string except at the beginning or end.

    (i) [0-9]?*[!A-Za-z]

    (ii) [!.]??*

    (iii) ?\*2004\*?


04. Explain what these wild-card patterns match: (i) `[A-z]????*` (ii) `*[0-9]*` (iii) `*[!0-9]` (iv) `*.[!s][!h]`

    (i) A filename comprising of at least 5 characters, where the first character is an alphabet or one of `` [, \, ], ^, _, ` `` characters.

    (ii) A filename comprising of at least one numeric character.

    (iii) A filename which doesn't end with a numeric character.

    (iv) A filename with a single character extension which is not `s` or `h`.


05. Devise a command that copies all files named chap01, chap02, chap03 and so forth, and up to chap26 to parent directory. Can a single wild-card pattern match them all?

    `cp chap[0][1-9] chap[1][0-9] chap2[0-6] ../`.

    No.


06. Explain what the commands **ls .\*** and **ls \*.** display.

    **ls .\*** lists all the hidden files in the current directory. If there are hidden sub-directories, their contents are listed.

    **ls \*.** lists all the non-hidden files and directories whose name ends with a dot.


07. You have a file named * and a direcotry named My Documents in the current directory. How do you remove them?

    By executing the `rm -rf My\ Documents ./*` command.


08. Explain the significance of single and double quoting when one is preferred to the other.

    Single and double quoting suppresses the special meaning of metacharacters and treats them literally. Double quoting is preferred when shell variable evaluation or command substitution is desired within the quoted string.


09. How do the commands **wc foo** and **wc < foo** differ? Who opens the file in each case?

    **wc foo** reads the file foo and displays the character count on the standard output.

    **wc < foo** reads the stream input coming from the file foo and displays the character count on the standard output.

    The command **wc** opens the file in the former case and the shell opens the file in the latter.


10. You want to concatenate two files, foo1 and foo2, but also insert some text after foo1 and before foo2 from the terminal. How will you do this?

    By runnning the command: `cat foo1 - foo2`


11. What happens when you use (i) **cat > foo** if foo contains data, (ii) **who >> foo** if foo doesn't exist, (iii) **cat foo > foo**, (iv) **echo 1> foo**?

    (i) The contents of foo are overwritten by the text entered on the terminal.

    (ii) file foo is created and the output of who is written into it.

    (iii) foo is blanked out.

    (iv) foo is blanked out.


12. Execute the command **ls > newlist**. What interesting observation can you make from the contents of **newlist**?

    newlist is present in the list of files alongwith other files listed as an output of ls command. newlist finds its way into the list as the shell opens the file before ls command comes into action.


13. What are _file descriptors_ and why is 2> used as the redirection symbol for standard error?

    _file descriptors_ are unique integer numbers assigned to open files (or rather byte streams) by the UNIX kernel.

    2> is used as redirection symbol for standard error because 2 is the default file descriptor for Standard Error stream.

14. Explain why the error message is seen on the terminal in spite of having used the 2> symbol:  

    $ **cat < foo 2>bar**  
    ksh: cannot open foo: No such file or directory  

    The error is thrown not by cat command but the shell. Any error thrown by cat command will be redirected to the file bar. Since here the command doesn't get to act and the shell itself fails to locate the file foo, hence the error.


15. What are the conditions that need to be satisfied to make this sequence work?  
    prog1 | prog2 | prog3

    Three conditions needs to be satisfied here. prog1 should send its output to Standard Output stream. prog2 should read its input from Standard Output of prog1 and write its output to Standard Output. prog3 should read its input from Standard Output of prog3 and write its output to Standard Output.


16. How do you find out the number of users logged in?

    `who | wc -l`


17. Use command substitution to print the (i) calendar of the current month, (ii) listing of a group of filenames stored in a file.

    (i) By running the command: ``echo "`cal`"``

    (ii) By running the command: ``echo "`cat list`"``


18. How will you store in a variable count (i) the total size of all C source files(.c), (ii) the total number of lines in a file?

    (i) By running `x=$(cat *.c | wc -c)` on terminal.

    (ii) By running `y=$(cat foo | wc -l)` on terminal.


19. A file foo contains a list of filenames. Devise a single statement, with suitable explanation, that stores in a variable count the total character count of the contents of these files. (HINT: Both command substitution and **cat** have to be used twice.)

    By running the command `count=$(cat foo | wc -m)`
