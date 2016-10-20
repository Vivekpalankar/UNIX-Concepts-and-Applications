## Errata


### Preface

-   Throughout the book Linux is referred to as an important Unix implementation. Although Linux is generally referred to an operating system, technically it is an operating system kernel. A kernel, despite being a very important component doesn't form a complete usable system. Unix utilities written as a part of [Free Software Foundation's](http://www.fsf.org/) [GNU](https://www.gnu.org/) project are often bundled with [Linux kernel](https://www.kernel.org/) to form a usable operating system distribution. Thus, it will be more appropriate to call the resulting system as [GNU/Linux](https://www.gnu.org/gnu/linux-and-gnu.en.html).


### Chapter 1 Getting Started

-   Page 17, Section 1.6, first paragraph. _Stallman runs the Free Software Foundation (formerly known as GNU - a recursive acronym that stands for "GNU's Not Unix!")._ The statement is misleading. Stallman founded Free Software Foundation (FSF) to support the free software movement and GNU is a free Unix-like operating system developed by FSF.

-   Page 17, Section 1.6, first paragraph. _Many of the important Linux tools were written and supplied free by GNU._ The statement is slightly misleading. Contrary to the common perception, Linux is not an operating system. Linux project is aimed at creating an operating system kernel. Utilities created as a part of GNU project are often bundled with Linux kernel to form an Operating System distribution which is correctly called as GNU/Linux distribution. So it would be more appropriate to say, _Many of the free software tools written as part of the GNU project are often bundled with Linux kernel and made available as GNU/Linux operating system distribution._

-   Page 19, Wrap Up, last note. _Linux is a UNIX implementation that is constantly growing with contributions from the Free Software Foundation (formerly, GNU)._ Couple things of note here. Linux isn't dependent on the said contributions as it's an independent project. Secondly, Free Software Foundation wasn't formerly called GNU as discussed above.

-   The answer for question 1.6 under Test Your Understanding is partial. The command **ls | wc -l** prints the count of non-hidden files and directories in the current directory.


### Chapter 2 The UNIX Architecture and Command Usage

-   Page 42, Wrap Up, last note. _Use the section number when a keyword is not found in Section 1._ should be corrected to, _Use the section number when a keyword is found in more than one Section._

-   The answer for question 2.3 under Test Your Understanding needs a slight correction. _The shell scans the command for some..._ should be read as _The shell scans the command-line for some..._.

    _It then passes on the command to the..._ should be read as _It then passes on the command-line to the..._.

-   The answer for question 2.12 under Test Your Understanding is partial. An option is also an argument but generally begins with a hyphen. It's given a special name because the list of options for a command is predetermined.


### Chapter 3 General-Purpose Utilities


### Chapter 4 The File System

-   The answer for question 4.3 under Test Your Understanding is partial. Two files named note and Note can coexist in the same directory only if the underlying file-system on disk is case sensitive.


### Chapter 5 Handling Ordinary Files

-   Page 85, Section 5.3, second paragraph. First sentence reads: "You have already seen (5.3) how the UNIX system". It should be read as: "Later you will see (5.3) how the UNIX system".

-   Page 100, Section 5.16, second paragraph. First sentence reads: "Only one these key options". It should be read as : "Only one of these key options".


### Chapter 6 Basic File Attributes


### Chapter 7 The vi Editor

-   Page 123, In **Figure 7.2 The Three Modes**, the key to switch from Command Mode to Input Mode shows `I` twice. It should be `i, I` and not `I, I`.


### Chapter 8 The Shell

-   The answer for question 8.5 under Test Your Understanding contains a typo. "3 has a higher value than e in the ASCII" should be replaced with "3 has a higher value than h in the ASCII".

-   For question 8.12 under Test Your Understanding, a possibly easier solution would be running the following command: `rm ./-foo`.


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

