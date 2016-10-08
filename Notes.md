## Notes

Chapter wise notes


### Preface

-   **foo** and **bar** are used as generic file and directory names.


### Chapter 1 Getting Started

-   Spaces around redirection (<, >) and piping (|) shell operators are irrelevant.


### Chapter 2 The UNIX Architecture and Command Usage

-   More than one command can be specified in a command line by seperating each one of them with a `;` character.

-   A sequence of one or more commands in a command-line can be grouped using parentheses.

-   To determine if a utility (also) exists as a shell builtin command, execute `type <command name>`. If it (also) exists as a shell builtin command, it will take precedence over the external one.

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

-    None of the above key sequences are standardised and may behave differently on different systems.


### Chapter 3 General-Purpose Utilities


### Chapter 4 The File System

-   Type `cd -` is a handy shortcut to switch to the last accessed directory.

-   UNIX file system is case sensitive. However, the default installation of macOS operating system uses a case insensitive HFS file system and hence disallows creating files having same name with differing case.

-   In macOS, if a file or directory has extended attributes, the permissions field printed by the `ls -l` command is followed by a '@' character.  Otherwise, if the file or directory has extended security information (such as an access control list), the permissions field is followed by a '+' character.


### Chapter 5 Handling Ordinary Files

-   When running `cp -R <source_file> <destination_file>`, if the `<source_file>` designates a directory, **cp** copies the directory and the entire subtree connected at that point. If the `<source_file>` ends in a _/_, the contents of the directory are copied rather than the directory itself.

-   The `rm` utility removes symbolic links, not the files referenced by the links.

-   Line ending character used across different operating systems:  

        macOS/ UNIX     (LF)    (\n)  
        Classic Mac OS  (CR)    (\r)  
        Windows         (CRLF)  (\r\n)


### Chapter 6 Basic File Attributes

-   `ls` command has no option to display only directories.


### Chapter 7 The vi Editor

-   Press `[Ctrl-w]` to erase an entire word.
-   Press `[Ctrl-l]` in command mode to redraw screen.
-   Enter `/` in input mode. Then press `[Esc]` and enter `70a*[Esc]` to enter _*_ 70 times.
-   Press `[Ctrl-p]` for string completion. The matches are cycled. To cycle backwards press `[Ctrl-n]`.
-   10 ways to enter Input mode from command mode:  

        i     Insert text to left of cursor (existing text shifed right)
        a     Append text to right of cursor (existing text shifted right)
        I     Inserts text at beginning of line (existing test shifted right)
        A     Appends text at the end of line
        o     Opens line below
        O     Opens line above
        rch   Replaces single character under cursor with _ch_ (No [Esc] required)
        R     Replaces text from cursor to right (existing text overwritten)
        s     Replaces single character under cursor with any number of characters
        S     Replaces entire line (the line is cleared)
-   `ZZ`: Command mode command to save the buffer and quit the editor.
-   Vim suggests appending a **!** to an ex mode command every time it feels that you could be doing something that is potentially unsafe. **!** is the universal overriding operator.
-   To temporarily exit to UNIX shell, enter `:sh` in ex mode, `:!cmd` runs shell command _cmd_.
-   vim understands a word as a navigation unit. A word in Vim consists of a string of alphanumeric characters including underscore (_).
-   Word navigation keys:  

        b     move back to beginning of word
        e     move forward to end of word
        w     move forward to beginning of word
-   `B`, `E`, `W` perform the same function, except that punctuations are skipped.
-   _-_ character counts as a word in tcp-ip.
-   `0` or `|` moves to beginning of line, _30|_ moves to column 30.
-   Shortcuts for scrolling in Command mode:  

        [Ctrl-f]    Scroll forward
        [Ctrl-b]    Scroll backward
        [Ctrl-d]    Scroll half page forward
        [Ctrl-u]    Scroll half page backward
-   Command mode navigation commands:  

        40G     goes to line 40         (ex mode equivalent :40)
        1G      goes to first line      (ex mode equivalent command :1)
        G       goes to end of file     (ex mode equivalent command :$)
-   `x` is the text deletion command. The character under the cursor gets deleted, and the text on the right shifts left to fill up the space. If the cursor is at the end of line, next line is not pulled up, rather the characters to left are deleted.
-   The deletion of text towards left is handled by `X` command. Keep it pressed to delete all text to the beginning of the line.
-   `J` join the current line and the line following it.
-   The three commands, `/` (search), `n` (repeat search) and `.` (repeat last editing command), form a wonderful trio of search - search-repeat - edit-repeat commands. You'll often be tempted to use this trio in many situations where you want the same change to be carried out at a number of places. For instance, if you want to replace some occurances of int with double, then first search for int with `/int`, change int to double with `3s`, repeat the search with `n`, and press `.` whenever you want the replacement to take place. To exclued embedded matched like printf, use regular expressions.
-   To startup vim by specifying a pattern, use the `+/` symbol before the pattern. E.g. To open file named _notes_ with the cursor station on the line containing the first occurance of the word _UNIX_, enter: `vim +/UNIX notes` as command line.
-   The syntax for subtitution in vim is `:s` (s comes after specifying the address part):  
        `:address/source_pattern/target_pattern/flags`  

    -   Address can be one or a pair of numbers separated by commas.

    -   The most comman flag is `g` which carries out the substitution for all occurances of pattern in a line.

    -   % can be used instead of 1,$ for address.

    -   If target pattern is left out, occurances of source pattern are deleted.

    -   If `g` flag is left out, the substituion is carried out for the first occurance in each addressed line.

    -   Add c in flag for inteactive substitution `gc`
        -   `y` confirms substitution
        -   `n` denys substitution
        -   `q` aborts substitution
        -   `a` makes substitution non-interactive


### Chapter 8 The Shell

-   The shell is a multi-faceted program. It's a command interpreter, a programming language and a process that creates environemnt for users to work in all rolled into one.

-   List of valid shell wild-cards:  

        *               Any number of characters including none
        ?               A single character
        [ijk]           A single character `i, j or k`
        [x-z]           A single character that is within the ASCII range of characters x-z inclusive
        [!ijk]          A single character that is not `i, j or k`
        [!x-z]          A single character that is not within the ASCII range of x-z inclusive
        {pat1, pat2...} pattern 1, pattern 2, etc.

        Note: When specifying range using character class, a valid range has lower ASCII value for character on the left than on the right.
        Note: In character class, negation can be performed only for a single character, not a string.

-   `*` and `?` don't match a filename beginning with a dot but can match any number of embedded dots. Also they can't match embedded `/` in a pathname.

-   `*` and `?` lose their meaning when used inside character class and are matched literally. Similarly `-` and `!` lose their meaning when used outside the class.

-   Escaping: Providing a `\` (backslash) before the wild-card to remove (escape) its special meaning.

-   Quoting: Enclosing wild-card(s) within quotes to supress its special meaning. When there are too many characters to escape, quoting can be a handy solution.

-   Shell uses space character to delimit command line arguments. It needs to be escaped using `\` (backslash).

-   Use backslash to escape a newline character, eg. when splitting a command line into multiple lines.

-   Doublequote don't protect dollar ($, variable prefix) and backquote (`, command substitution) characters. Single quote protects all special characters. Double quotes protects single quotes and vice versa.

-   The shell makes available three special files. These special files are actually **streams** of characters which many commands see as input and output. A stream is simply a sequence of bytes. Each stream is associated with a default device.  

        Standard Input:     The file (or stream) representing input, which is connected to the keyboard.
        Standard Output:    The file (or stream) representing output, which is connected to the display.
        Standard Error:     The file (or stream) representing error messages that emanate from the command or shell. This is connected to the display.

-   Every command that uses streams will always find these files open and available. The shell associates each of these files with a default physical device. The shell can easily unhook a stream from its default device and connect it to a disk file (or to any command).

-   Shell manipulates default source and destination of streams to implement _redirection_ and _pipelines_.

-   Question under Note on page 157 reads, **Any idea what cat foo > foo does?** The shell opens foo for writing, hence clearing its contents. Following that cat opens foo for reading, finds nothing and then writes nothing to foo. Thereby clearing the contents of the file foo.

-   Each open file in system is represented by a number called file descriptor. A file is opened by referring to its filename, but subsequent read and write operations identify the file by this file descriptor. Kernel maintains a table of file descriptors for every process running in the system. The first three slots are allocated to the three standard streams:  

        0   Standard Input
        1   Standard Output
        2   Standard Error

-   These descriptors are implicitly prefixed to the redirection symbols. `>` and `1>` mean the same thing. `<` and `0<` are also identical.

-   POSIX form requires a command to be inside () following a $ sign.

-   All the shell variables are of string type.

-   After command line is terminated by hitting [Enter], the shell goes ahead with processing the command line in one or more passes:  

        Parsing:                    Breakup command-line into words.
        Variable evaluation:        All $-prefixed strings are evaluated.
        Command substitution:       Commands surrounded by backticks are executed.
        Redirection:                Shell opens appropriate files.
        Wild-Card interpretation:   Expanded into sorted list of filenames matching the pattern.
        PATH evaluation:            Searching for the command executable file in a predetermined list of directories.


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

