## Flex Your Brain

01. Describe the contents of a directory, explaining the mechanism by which its entries are updated. Why is the size of a directory usually small?

    A directory is technically a file that contains the name and the inode number of the files and sub-directories it houses. The entries in a directory are updated by the kernel on the users behalf when new files and sub-directories are added or removed.

    The size of a directory is usually small as it doesn't actually store the files and sub-directories it houses, just their name and inode numbers.


02. What is the difference between **cat foo** and **cat > foo**? Why do you have to use [Ctrl-d] in one and not in the other?

    **cat foo**: Displays the contents of the file **foo** on the terminal.

    **cat > foo**: Doesn't return the prompt and let the user type any text. On encountering end-of-file `[Ctrl-d]` character, the entered text is saved in a file named **foo** in the current directory.

    Use of `[Ctrl-D]` character is required when entering the text from standard input to let the shell know that the text entry is over.


03. Will the command **cp foo bar** work if (i) foo is an ordinary file and bar is a directory, (ii) both foo and bar are directories?

    1.  Yes. The file **foo** will be copied into the directory **bar**.

    2.  No. An error message is displayed stating **foo** is a directory and is not copied.


04. Assuming that bar is a directory, explain what the command **rm -rf bar** does. How is the command different from **rmdir bar**?

    The command **rm -rf bar** will delete directory **bar** along with all the files and sub-directories recursively, disregarding the write protection status of any file or sub-directory and non-emptiness of any sub-directory.

    The command **rmdir bar** will work only when the directory is not write-protected and is completely empty.


05. What is the significance of these commands? (i) **mv $HOME/include .** (ii) **cp -r bar1 bar2** (iii) **mv * ../bin**

    1.  **mv $HOME/include .**: The file or directory named _include_ present in the logged in users home directory is moved to the current working directory. The command fails if the user is currently in the home directory.

    2.  **cp -r bar1 bar2**: Recursively copy the contents of **bar1** to **bar2**. If **bar2** exists, Recursively copy contents of **bar1** into **bar2**, thus making the copy of **bar1** a sub-directory of **bar2**.

    3.  **mv * ../bin**: Move all the files and directories in the current directory into a directory named **bin** in the parent directory. The command fails if the directory **bin** doesn't exist.


06. The command **cp hosts backup/hosts.bak** didn't work even though all files exist. Name three possible reasons.

    1.  Read permission not available for the file **hosts**.

    2.  Write permission not available for the file **hosts.bak**.

    3.  Execute permission not available for the directory backup.


07. You have a directory structure $HOME/a/a/b/c where the first a is empty. How do you remove it and move the lower directories up?

    By executing the following command line:  

    `cd ; mv a temp ; mv temp/a . ; rmdir temp`

    Change to the home directory. Then, first rename the directory _a_ under home directory to something other than _a_, say _temp_. Then move the directory _a_ under _temp_ directory to the current directory i.e. the home directory. Then remove the _temp_ directory normally as it is empty.


08. Explain the significance of the repeat factor used in **more**. How do you search for the pattern include in a file and repeat the search? What is the difference between this repeat command and the dot command?

    Using repeat factor, an internal command can be repeated _n_ number of times.

    Type `/include` to locate the first occurrence of the pattern. Continue pressing the key `n` to repeat the search for the occurrences on further pages.

    Using repeat factor, a command can be executed for a fixed number of times. The dot command on the other hand simply repeats the last command.


09. A file with the .ps extension should be a Postscript file, but how can you be sure? What is the importance of this file type in the printing subsystem?

    We can ensure that a the file is indeed Postscript file by using `file` command and checking the type.

    Postscript files are properly formatted for input to Postscript printers.


10. A file foo contains a list of filenames, with one filename in each line. One of the filenames appears to have an embedded space. How will you (i) count the number of filenames, (ii) check whether there's actually an embedded space in a filename?

    1.  We can count the number of filenames using `wc -l` command. This command outputs the total number of lines in the file.

    2.  By displaying the octal dump of the files contents using the command `od -bc foo` and verifying the presence of a space character (ASCII value of space character is 040 in octal).


11. How do DOS and UNIX text files differ? Name the utilities that convert files between these two formats?

    DOS and UNIX text files differ by using different line ending characters. DOS uses the combination of _carriage return_ and _line feed_ characters (\r\n). Whereas, UNIX uses _line feed_ (\n).

    **dos2unix** command converts a text file from DOS format to UNIX format by removing the extra carriage return characters from the places where the line ending character combination occurs. **unix2dos** command reverses the process by appending the carriage return character before every occurrence of line feed character.


12. You have two lists, foo1 and foo2, containing names of users. How do you create a third list of those users in foo2 who are absent in foo1? When will the command not work properly?

    The required list can be created by executing the command `comm -13`, which will list entires unique to file foo2.

    The command will not work properly when the files are unsorted or the files contains more than one name per line.


13. How do you use **tar** to add two files, foo.html and bar.html, to an archive and then compress the archive? How will you reverse the entire process and extract the files in their original uncompressed form?

    To add the two files to an archive and compress the archive, run the command: `tar -cvf archive.tar foo.html bar.html ; gzip archive.tar`. The compressed archive will be saved as _archive.tar.gz_.

    To reverse the process, uncompress and unarchive the file by running the command: `tar -xvf archive.tar.gz`. This can be followed by deleting the compressed archive by running the command `rm archive.tar.gz`, to completely reverse the process.


14. Name three advantages **zip** has over **gzip**. How do you use **zip** to send a complete directory structure to someone by email? How does the recipient recreate the directory structure at her end?

    zip files can he handled easily both in Windows and UNIX. zip combines archiving and compressing under a single command. zip command provides facility to add/append files to an existing compressed archive.

    To compress and archive a directory hierarchy to send via email run the command: `zip -r archive.zip direcotry_path`.

    The recipient can easily recreate the directory structure by running the command: `unzip archive.zip`.


15. What is meant by _recursive_ behavior of a command? Name four commands, along with a suitable example of each, that can operate recursively.

    A command behaves recursively when it can descent a directory structure and examine and run over all the files and sub-directories and files thereof. 

    Examples of commands which support recursive operation:

    -   `cp` command with `-R` option can recursively copy a directory hierarchy.

    -   `rm` command with `-r` option can recursively delete files in a directory hierarchy.

    -   `ls` command with `-R` option can recursively list files in a directory hierarchy.

    -   `zip` command with `-r` option can recursively compress and archive a directory hierarchy.
