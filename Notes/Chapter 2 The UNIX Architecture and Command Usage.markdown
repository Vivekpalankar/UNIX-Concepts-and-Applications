## Notes

-   More than one command can be specified in a command-line by separating them with a `;` character.

-   A sequence of one or more commands in a command-line can be grouped using parentheses.

-   To determine if a utility (also) exists as a shell built-in command, run `type utility`. If it (also) exists as a shell built-in command, it will take precedence over the external one.

-   Manual page for a command can be located on disk by executing `man -w <command name>`.

-   Similar looking commands `whereis` and `which` have a subtle difference. `whereis` checks only standard binary directories, while `which` searches all the directories specified in the _PATH_ environment variable sequentially and displays the first match found. `which -a` prints all the matches found, in the order they are encountered in PATH.

-   Both `apropos` and `whatis` command search the _whatis_ database for a match. While `whatis` only matches complete words, `apropos` also lists partial matches. As such `whatis` should be preferred over `apropos`, as the latter may return irrelevant results.

-   `[Ctrl-c]` kills a command-line or interrupts a command in execution.

-   `[Ctrl-i]` generates `[Tab]` character on the terminal.

-   `[Ctrl-h]` erases character just like `[Backspace]` key.

-   `[Ctrl-u]` is the line-kill character. It erases everything in the line and returns the cursor to the beginning of the line.

-   `[Ctrl-d]` is the _eof_ or _end-of-file_ character. It is also used to terminate the input from the terminal or to logout from current session.

-   `[Ctrl-s]` stops scrolling of the screen output.

-   `[Ctrl-q]` resumes scrolling of the screen output.

-   `[Ctrl-j]` and `[Ctrl-m]` key sequence generate _linefeed_ and _carriage return_ characters, respectively. Either one of them can be used in place of `[Enter]` key in the shell.

-    None of the above key sequences are standardized and may behave differently on different systems.
