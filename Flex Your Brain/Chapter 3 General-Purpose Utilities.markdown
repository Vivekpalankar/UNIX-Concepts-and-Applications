## Flex Your Brain

01. How do you display both date and time in the format _dd-mm-yy/hh:mm:ss_?

    By running the following command:  

    `date +"%d-%m-%y/%H:%M:%S"`


02. What is an escape sequence? Name three escape sequences used by the **echo** command, and explain the significance of each.

    An escape sequence is generally a two character-sequence beginning with a backslash (`\`) character.

    Three escape sequences used by echo command, with their significance are:

    `\n` - Prints a newline.

    `\b` - Prints a backspace character, i.e. removes the previous character.

    `\\` - Prints a literal backslash character.


03. The command **echo "Filename: \c"** didn't place the cursor at the end of the line. How will you modify the command to behave correctly if your shell is (i) Bash, (ii) anu other shell?

    (i) Supplying -e option to echo command as: `echo -e "Filename: \c"`

    (ii) Supplying -n option to echo command as: `echo -n "Filename: \c"`


04. Why doesn't this command run in the way it is meant to? **printf "Filename: %s\n", fname**

    The comma character is not required after the first argument. If fname needs to be evaluated as a variable it should be preceded by $ character. The altered command line would read:

    `printf "Filename: %s\n" $fname`


05. Convert the decimal number 192 to octal and hexadecimal using (i) **bc** and (ii) **printf**. Which one will you use to display the number in binary?

    (i) obase=8  
        192

        obase=16  
        192

    (ii) printf "The value of 192 in octal is %o and hexadecimal is %x\n" 192 192


06. Run **ps**, the **script** command run **ps** again. What do you notice?

    Running ps command spawns a sub-shell.


07. In what way is the **mailx** command superior to a GUI program like Netscape or Mozilla?

    mailx can obtain values it's for arguments via shell variables or at runtime, can work non-interactively and can be automated.


08. Explain the significance of the terms _mailbox_ and _mbox_.

    When a new email message is received, it is stored in a file referred to as _mailbox_. Once the email message is read, it automatically moves to a file named _mbox_ which is generally stored in the users home directory.


09. You need to accept a secret code through shell script. What command will you run in the script to make sure that your keyboard input is not displayed? How do you then revert to the normal setting?

    Executing `stty -echo` command will turn off display of keyboard input.

    Setting can be reverted by executing `stty echo` command.


10. Both your local and remote machines use identical versions of UNIX. How do you confirm whether you are logged on to a remote machine or not?

    By running `uname -n` and displaying the hostname.


11. How do you determine the erase, kill and eof characters on your system?

    By examining the output of `stty -a` command and reading values corresponding to _erase_, _kill_ and _eof_ keys.


12. What will you do to ensure that [Ctrl-c] interrupts any program? Will it work the next time you log in?

    By setting [Ctrl-c] corresponding to _kill_ keyword using stty command as: `stty kill \^c`.

    No. The settings doesn't persist between login sessions.