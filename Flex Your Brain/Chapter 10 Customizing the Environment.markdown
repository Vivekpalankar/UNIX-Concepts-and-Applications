## Flex Your Brain

01. What is the difference between an _interactive_ and _non-interactive_ shell? Which features of the shell have significance only in an interactive shell?

    


02. Why are all environment variables represented in a fixed format regardless of the shell you use?

    


03. Which two environment variables are set by reading `/etc/passwd`?

    


04. Explain the significance of the MAIL and MAILCHECK variables. How do you come to know that mail has arrived?

    


05. Mention the steps needed to (i) change the prompt to look like this: `[jupiter-henry ~/project8]` (user - henry, machine name - jupiter and current directory - project8) (ii) revert to your original prompt.

    


06. Create an alias named **rm** that always deletes files recursively. How can you execute the original **rm** command without unaliasing it?

    


07. How can you prevent your files from being overwritten using the redirection symbols in Korn and Bash? How will you overwrite these files?

    

08. What is the significance of these commands in Bash? (i) **!50** (ii) **!-2:p** (iii) **!!** (iv) **^doc^bak**. What are their equivalents in Korn?

    


09. In the Korn shell, the command **r ca** runs from the history list (i) the last command having ca embedded. (ii) the first command beginning with ca. (iii) the last command beginning with ca. (iv) all commands beginning with ca.

    


10. Can you condense these sequences? (i) **cp *.c c_progs ; cd c_progs** (ii) **cmp foo foo.bak ; cmp foo foo.doc**

    


11. Using the history facility, how can you repeatedly execute this sequence in (i) Korn, (ii) Bash? **vi signal.c ; cc signal.c**

    


12. You want to recall all the **tar** commands that you executed for viewing. How can you see them in turn by pressing a single key repeatedly in Korn and Bash?

    


13. Explain the significance of these commands: (i) **cd ~henry** (ii) **cd ~/henry** (iii) **cd ~-** (iv) **cd -**

    


14. Why do all shells use a profile as well as an rc file? What type of entries do you place in each?

    


15. How can you make all aliases placed in ~/.alias available in all sub-shells? Will the aliases be available in a shell script in (i) Korn (ii) Bash?

    


16. Name two ways of making the changes made to .profile available in the environment.

    
