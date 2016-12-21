## Flex Your Brain

01. Mention the significance of the two shell parameters, $$ and $!.

    


02. Mention the similarities that you find between processes and files.

    


03. What are the two options available to a parent after it has spawned a child? How can the shell be made to behave in both ways?

    

04. Explain what daemon processes are and their behavioral pattern. Name three examples of daemons and the tasks they perform. How do you identify these processes?

    


05. How is a process created? Mention briefly the role of the fork-exec mechanism in process creation.

    


06. Name five important process attributes that are inherited by the child from its parent.

    


07. Unlike the built-in commands, **pwd** and **echo**, which also exist as separate disk files, why is there no file named **cd** on any UNIX system?

    


08. Explain the sequence of steps followed by **init** that allows us to log in and work at the shell prompt. What does **init** do when a user logs out?

    


09. What is a zombie, and how is it killed?

    


10. What is the difference between a process run with & and one run with **nohup**?

    


11. What are signals? Name a way of generating a signal from the keyboard. Why should we use **kill** with signal names rather than their numbers?

    


12. Explain whether the following are true or false: (i) A script can be made to ignore all signals. (ii) THe parent process always picks up the exit status of its children. (iii) One program can give rise to multiple processes.

    


13. The **jobs** command issued the message `jobs: not found`. When does that normally happen?

    


14. What is the difference between a job and a process? How do you (i) suspend the foreground job, (ii) move a suspended job to the background, (iii) bring back a suspended job to the foreground?

    


15. Interpret these `crontab` entries and explain if they will work: (i) `* * * * * dial.sh` (ii) `00-60 22-24 30 2 * find.sh`

    


16. Frame a crontab entry to execute the connect.sh script every 30 minutes on every Monday, Wednesday and Friday between the times 8 a.m. and 6 p.m.

    
