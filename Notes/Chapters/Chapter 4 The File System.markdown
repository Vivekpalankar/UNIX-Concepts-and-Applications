## Notes

-   Unlike DOS files, a UNIX file doesn't contain an end-of-file mark.

-   A file name may consist of almost any ASCII character except the / and the NULL character. It is highly recommended to use restrict filenames to use alphanumeric, dot (.), hyphen (-) and underscore (_) characters.

-   `~` refers to currently logged in users home directory. ~username refers to home directory of user named _username_.

-   `cd -` is a handy shortcut to switch to the last accessed directory.

-   UNIX file system is case sensitive. However, the default installation of macOS operating system (as of macOS 10.12) uses a case insensitive HFS file-system and hence disallows creating files having same name with differing case.

-   In macOS, if a file or directory has extended attributes, the permissions field printed by the `ls -l` command is followed by a `@` character.  Otherwise, if the file or directory has extended security information (such as an access control list), the permissions field is followed by a `+` character.
