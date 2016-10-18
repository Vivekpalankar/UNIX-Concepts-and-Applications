## Notes

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
