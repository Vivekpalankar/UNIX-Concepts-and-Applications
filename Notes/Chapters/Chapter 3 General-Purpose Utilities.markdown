## Notes

-   An escape sequence is a multi-character string (generally two), beginning with a backslash and treated as a single character.

-   `[Ctrl-g]` represents the bell character.

-   Bash interprets the escape sequence for `echo` command when used with `-e` option.

-   Some commonly used escape sequences are:

        \a      Bell
        \b      Backspace
        \c      No newline (cursor in same line)
        \f      Form-feed
        \n      Newline
        \r      Carriage return
        \t      Tab
        \v      Vertical tab
        \\      Backslash
        \0n     ASCII character represented by the octal value n, where n can't exceed 0377 (decimal value 255)

-   `printf` command is a POSIX compliant and its use is recommended over `echo` command.

-   Use `stty` command to display and set terminal attributes.
