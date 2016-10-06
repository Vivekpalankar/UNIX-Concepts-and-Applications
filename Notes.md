## Notes

Chapter wise notes


### Preface

-   **foo** and **bar** are used as generic file and directory names.


### Chapter 1 Getting Started

-   Spaces around redirection (<, >) and piping (|) shell operators are irrelevant.


### Chapter 2 The UNIX Architecture and Command Usage

-   More than one command can be specified in a command line by seperating each one of them with a `;` character.

-   A sequence of one or more commands in a command-line can be grouped using parentheses.

-   To determin if a command (also) exists as a builtin command execute `type <command name>`. If it exists as a shell builtin command, it will take precedence over the external one.

-   Manual page for a command can be located on disk by executing `man -w <command name>`.

-   Similar looking commands `whereis` and `which` have a subtle difference. `whereis` checks only standard binary directories, while `which` searches all the directories specified in the _PATH_ environment variable sequentially and displays the first match found. `which -a` prints all the matches found.

-   Both `apropos` and `whatis` command search the _whatis_ database for a match. While `whatis` only matches complete words, `apropos` also lists partial matches. As such `whatis` should be preferred over `apropos`, as the latter may return irrelevant results.

-   [Ctrl-c] kills a command-line or interrupts a command in execution.

-   [Ctrl-i] generates [Tab] character on the terminal.

-   [Ctrl-h] erases character just like [Backspace] key.

-   [Ctrl-u] is the line-kill character. It erases everything in the line and returns the cursor to the beginning of the line.

-   [Ctrl-d] is the _eof_ or _end-of-file_ character. It is also used to terminate the input from the terminal or to logout from current session.

-   [Ctrl-s] stops scrolling of the screen output.

-   [Ctrl-q] resumes scrolling of the screen output.

-   [Ctrl-j] and [Ctrl-m] key sequence generate _linefeed_ and _carriage return_ characters, respectively. Either one of them can be used in place of [Enter] key in the shell.

-    None of the above key sequences are standardised and may behave differently on different systems.


### Chapter 3 General-Purpose Utilities


### Chapter 4 The File System

-   Type `cd -` is a handy shortcut to switch to the last accessed directory.

-   UNIX file system is case sensitive. However, the default installation of macOS operating system uses a case insensitive HFS file system and hence disallows creating files sharing name with differing case.

-   In macOS, if a file or directory has extended attributes, the permissions field printed by the -l option is followed by a '@' character.  Otherwise, if the file or directory has extended security information (such as an access control list), the permissions field printed by the -l option is followed by a '+' character.


### Chapter 5 Handling Ordinary Files

-   When running `cp -R <source_file> <destination_file>`, if the _source\_file_ designates a directory, **cp** copies the directory and the entire subtree connected at that point. If the _source\_file_ ends in a _/_, the contents of the directory are copied rather than the directory itself.

-   Line ending character used across different operating systems:  

        macOS/ UNIX     (LF)    (\n)  
        Classic Mac OS  (CR)    (\r)  
        Windows         (CRLF)  (\r\n)


### Chapter 6 Basic File Attributes

-   _ls_ command has no option to display only directories.


### Chapter 7 The vi Editor


### Chapter 8 The Shell


### Chapter 9 The Process


### Chapter 10 Customizing the Environment


### Chapter 11 More File Attributes


### Chapter 12 Simple Filters


### Chapter 13 Filters Using Regular Expressions - grep and sed


### Chapter 14 Essential Shell Programming


### Chapter 15 Essential System Administration


### Chapter 16 The X Window System


### Chapter 17 Networking Tools


### Chapter 18 awk - An Advanced Filter


### Chapter 19 perl - The Master Manipulator


### Chapter 20 Advanced vi


### Chapter 21 Advanced Shell Programming


### Chapter 22 Program Development Tools


### Chapter 23 Systems Programming I - Files


### Chapter 24 Systems Programming II - Process Control


### Chapter 25 Advanced System Administration

