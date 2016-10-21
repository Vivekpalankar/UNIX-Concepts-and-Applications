## Flex Your Brain

01. Name the three modes of **vi** and explain how you can switch from one mode to another.

    The three modes of **vi** are: Command Mode, Input Mode and ex Mode (or Last Line Mode).

    The editor starts in Command mode by default. To switch to Input mode, enter one of _i, I, a, A, o, O, r, R, s or S_ key. To switch back to Command mode, press the `[Esc]` key. To enter ex mode, switch back to Command mode first if you are currently in Input mode, then press the _:_ key followed by ex mode command. ex mode command is executed by pressing the [Enter] key, which on completion switches the editor back to Command mode.


02. How will you add /* at the beginning of a line and */ at the end?

    First navigate to the desired line using appropriate navigation keys. Press `I` key to insert text at the beginning of the line. Enter `/*` characters and press [Esc] key to switch back to Command mode. Now press `A` key to append text at the end of the line. Enter `*/` characters and press the [Esc] key to switch back to the Command mode.


03. How do you remove the characters that you just inserted above without using the undo feature?

    Since the cursor is still placed at the last character of the line, press `x` twice to delete two characters at the end of the line. Now press `0` to move to the beginning of the line. Again press `x` twice to delete the two characters at the beginning of the line.


04. How do you move to line number 100 and then write the remaining lines (including that line) to a separate file?

    To move to line number 100, enter `:100`.

    To write the lines from that point onwards to the end of the file to a file named _newfile_, enter the ex mode command `:.,$w newfile`


05. **vi** refuses to quit with **:q**. What does that indicate and how do you exit anyway?

    This happens when there are unsaved changes in the buffer. To discard the unsaved changes and exit anyways, enter the ex mode command: `:q!`


06. Explain what the following commands do: (i) **:.,10w foo** (ii) **:$w! foo**. In which mode are the commands executed and what difference does it make if foo exists?

    (i) **:.,10w foo**: Saves the lines from the current line to 10th line below in a file named foo.

    (ii) **:$w! foo**: Saves the last line in a file named foo. Overwrite the file foo if it already exist.


07. Assuming that the cursor is at the beginning of the line, name the commands required to replace (i) `echo 'Filename: \c'` with `echo -n "Filename: "` (ii) `printf("File not found\n");` with `fprintf(stderr, "File not found\n");`

    (i) e, a, enter the characters: ` -n`, [Esc], w, r", 3e, 2x, r"

    (ii) i, enter the character: `f`, [Esc], w, a, enter the characters: `stderr, `, [Esc]


08. In the midst of your work, how can you see the list of users logged in? If you have a number of UNIX commands to execute, which course of action will you take?

    By running the who command by issuing ex mode command as `:!who`.

    Switch to shell without quitting the editor by issuing ex mode command as `:sh`. Quitting the shell will returns to the editor session.


09. Name the sequence of commands to execute to move to the line containing the string #include, deleting four lines there, and then placing the deleted lines at the beginning of the file.

    :/#include[Enter], 4dd, :1, P


10. Mention the sequence of commands to execute that will replace printf( with fprintf(stderr,? How will you repeat the action globally?

    :1,$s/printf(/fprintf(stderr,/g


11. How do **u** and **U** differ? When will **U** fail to work?

    In default configuration, `u` undoes the most recent, single editing change. Subsequent pressing of the key will redo the change.

    When a number of editing changes have been made to a single line, pressing `U` will discard all the changes made since the cursor was moved to the line.


12. Name the commands required to non-interactively replace all occurrences of cnt with count in (i) the first 10 lines, (ii) the current line, (iii) all lines. How do you repeat the exercise in an interactive manner?

    (i) `:1,10s/cnt/count/g`

    (ii) `:.s/cnt/count/g`

    (iii) `:1,$s/cnt/count/g`

    by changing the flag to `gc` from `g`.


13. If the power to the machine is cut off which a **vi** session is active, how does it affect your work? What salvage operation will you try?

    vi editor stores most of the unsaved buffer in a hidden swap file on disk. The file is automatically removed by the editor upon successful exit.

    If the same file is opened after a crash, the editor complains. In such a case, it is advised to use `:recover` ex mode command.


14. You made some changes to a read-only file and then find that you can't save the buffer. What course of action will you take without quitting the editor?

    Save the file under a different name after making sure that the file doesn't exist, using the command `:w filename`


15. Copy /etc/password to passwd. Name the **vi** commands required to save the first 10 lines in passwd1, the next 10 in passwd2 and the rest in passwd3.

    Copy the file in the home directory by running: `cd ; cp /etc/passwd .`

    Start the editor by running: `vi passwd`

    Subsequently enter the following ex mode commands one by one: `:1,10w passwd1`, `:11,20w passwd2`, `:21,$w passwd3`.


16. List the editing and navigation commands required to convert the following text:

        # include <errno.h>
        void quit (char *message)
        {
            printf("Error encountered\n");
            printf("error number %d, ", errno);
            printf("quitting program\n");
            exit(1);
        }

    to this:

        #include <stdio.h>
        #include <errno.h>
        void quit (char *message, int exit_status) {
            /* printf("Error encountered\n"); */
            fprintf(stderr, "Error number %d, quitting program\n", errno);
            exit(exit_status);
        }

    Enter the command sequence shown below as it is. Enter the characters as indicated

    :1, O, enter the characters: `#include <stdio.h>`, [Esc], j, 0, l, x, 6e, a, enter the characters: `, int exit_status`, A, enter the characters: ` {`, [Esc], j, dd, 0, w, i, enter the characters: `/* `, [Esc], A, enter the characters: ` */`, [Esc], j, 0, w, i, enter the character: `f`, [Esc], w, a, enter the characters: `stderr, `, [Esc], 2w, rE, 5w, i, enter the characters: `quitting program\n`, [Esc], j, dd, 0, 3w, s, enter the characters: `exit_status`, [Esc]
