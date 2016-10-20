## Flex Your Brain

01. Describe briefly the UNIX architecture explaining the role played by the kernel and shell in sharing the workload.

    The UNIX system divides the labor between two agencies - the _kernel_ and the _shell_. Kernel interacts with the machines hardware and the shell interacts with the user. Kernel is responsible for all sorts of system management activities. Shell performs the job of command interpretation and gets a command line executed with the help of the kernel.

    _File_ and _Process_ are two core entities present in a UNIX system. A file is an array of bytes and a process is a file in execution.

    UNIX kernel provides _system calls_ - C language routines which provides interfaces for communication to shell and other applications.


02. Explain briefly the significance of a UNIX file and the relation it has to a process. Why do UNIX systems predominantly use text files?

    Everything is represented in UNIX by a file which is just an array of bytes. A file when executed as a program is called a process. A file is stored on disk and a process exists in memory.

    UNIX systems predominantly use text file as they are easy to edit. A lot of programs (called scripts) are stored in their source form and can be directly executed by an interpreter. UNIX started out as an operating system targeted towards engineering community regularly tinkers with configuration parameters and program source code. Engineers also constantly create new program and share it with their peers. Using text file format makes all of these activities much easier. UNIX also provide a large collection of text manipulation tools to enable editing files without using an editor.


03. What do multiprogramming, multiuser and multitasking mean?

    Multiprogramming means keeping multiple programs in the system memory at the same time.

    Multiuser means ability to support multiple users at the same time and allowing them to use a single installation of UNIX simultaneously.

    Multitasking means ability to execute multiple tasks concurrently and even switch between them.


04. What are system calls and what role do they play in the system? How is C programming so different and powerful in the UNIX environment compared to Windows?

    System calls are special routines, written in C language and built into the kernel. They act as an interface to the kernel for shell and other programs. System calls are standardized across UNIX and any UNIX distribution by definition offers the same set of system calls.

    C programming is different and powerful in the UNIX environment as C was created and implemented first on UNIX and then the entire UNIX operating system, including all the utilities was written in C. Thus, C language and its standard library is deeply integrated into UNIX operating system. UNIX system calls are implemented in C and are offered as C function interfaces. Windows doesn't share the same system calls as UNIX, neither does it include the standard library in the default installation.


05. Why are many UNIX commands designed to perform simple rather than complex tasks?

    Creators of UNIX followed the _small is beautiful_ philosophy and never attempted to pack many features in small number of tools.
    Simple tools that perform well defined tasks can be combined with operators to perform complicated tasks and filter data.


06. The **wc** command was designed to count characters, lines and words _only_ in files. Explain whether the statement is true or not with a suitable example.

    **wc** command can be used with not just files but with input coming from _standard input_ or from output of some other command. This is illustrated with the following examples:

    Execute `wc` command without any argument. The command prompt won't return. Enter some text and terminate the input by entering a newline immediately followed by `eof` character using `[Ctrl-d]`. The output will represent count of the characters in the entered text.

    Pipe the output of some command such as `ls` to `wc -l` to count the number of non-hidden files and directories in the current directory. Enter the command line as : `ls | wc -l`.


07. Name three major differences between UNIX commands and Windows programs.

    UNIX commands are case sensitive unlike Windows.

    Windows commands works irrespective of the presence of whitespace between the command and its options unlike UNIX where whitespace is mandatory.

    UNIX commands makes use of POSIX systems calls whereas Windows don't.


08. A program file named foo exists in the current directory, but when we try to execute it by entering foo, we see the message `foo: command not found`. Explain how that can happen.

    This can happen when `foo` doesn't exist as a shell built-in command and is not present in any of the directories present in the list of directories stored in the _PATH_ environment variable. The latter case will happen if the current directory represented by `.` is not present in the PATH environment variable.


09. What is whitespace? Explain the treatment that shell metes out to a command that contains a lot of whitespace.

    Any contiguous sequence of space and tab characters is called a whitespace. If multiple contiguous whitespace is present between the command and it's arguments, the shell automatically compresses it to a single space.


10. If a command, filename and system call have the same name and are available in Sections 1, 5 and 2, how will you display the man pages of each one of them?

    By specifying the section number as a command argument as `man 1 <command>`, `man 5 <filename>` and `man 2 <system call>`. Alternatively, they all can be viewed in succession by passing `-a` argument to the man command.

    Note: On GNU/Linux, the equivalent commands are `man -s1 <command>`, `man -s5 <filename>` and `man -s2 <system call>`.


11. What do the | and the three dots in the SYNOPSIS section of these man pages indicate as shown below?

    `/usr/xpg4/bin/tail [ -f | -r ]`  
    `/usr/bin/ls [ -aAbcCdfFgilLmnopqrRstux1 ] [ file ... ]`  

    Either one of `-f` or `-r` can be used as an argument when executing the command `/usr/xpg4/bin/tail [ -f | -r ]`.

    The `file` argument can be repeated any number of times when executing the command `/usr/bin/ls [ -aAbcCdfFgilLmnopqrRstux1 ] [ file ... ]`.


12. Explain the significance of the interrupt and eof characters. With which keys are they associated on your system?

    Interrupt character represented by _[Ctrl-c]_ is used to interrupt a long running or an unresponsive program.

    eof character represented by _[Ctrl-d]_ can be used to terminate user input or to log out from the current session.


13. How do you direct **man** to use a specific pager, say, **less**?

    Update the PAGER environment variable to use the desired pager say **less** by running `PAGER=less` on shell prompt.
