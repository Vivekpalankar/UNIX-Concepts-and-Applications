## Notes

-   **foo** and **bar** are commonly used generic file and directory names.

-   Add an `&` to the end of a Bash command line to execute it in the background.

-   [Tab] key can be used in Bash for auto-completing a command or file name.

-   Bash keyboard shortcuts. Below mentioned sequences are not standardized and may behave differently on different systems.

    -   `[Ctrl-i]` generates `[Tab]` character on the terminal.

    -   `[Ctrl-h]` erases character just like `[Backspace]` key.

    -   `[Ctrl-u]` delete all the text to the left of the cursor.

    -   `[Ctrl-k]` delete all the text to the right of the cursor.

    -   `[Ctrl-w]` delete words to the left, one word at a time.

    -   `[Ctrl-y]` performs a paste (after performing `[Ctrl-u]`, `[Ctrl-k]` or `[Ctrl-w]`).

    -   `[Ctrl-d]` is the _eof_ or _end-of-file_ character. It is also used to terminate the input from the terminal or to logout from current session.

    -   `[Ctrl-s]` stops scrolling of the screen output.

    -   `[Ctrl-q]` resumes scrolling of the screen output.

    -   `[Ctrl-m]` and `[Ctrl-j]` key sequence generate _carriage return_ and _linefeed_ characters, respectively. Either one of them can be used in place of `[Enter]` key in the shell.

    -   `[Ctrl-l]` clears the terminal. `[Cmd-k]` on macOS clears the terminal completely (no scroll-back).

    -   `[Ctrl-a]` takes cursor to the start of the line.

    -   `[Ctrl-e]` takes cursor to the end of the line.

    -   `[Ctrl-r]` reverse search history.

    -   `!!` repeats last command.

    -   `[Ctrl-c]` kills a command-line or interrupts a command in execution.

    -   `[Ctrl-z]` suspends process and returns the shell prompt. Use **fg** command to resume job in foreground or **bg** in background. 

    -   `echo $?` displays the exit status of the last command.
