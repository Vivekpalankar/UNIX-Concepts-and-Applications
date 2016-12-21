## Flex Your Brain

01. What is context switching?

    


02. What is the role of Memory Management Unit in process switching. Why can't one process corrupt the address space of another?

    


03. Write a program that displays all environment variables.

    


04. Modify the program in 24.11 (Test Your Understanding) so that process A creates B and B creates C. The summation should be performed in C and the result returned to B as the exit status. B should double the summed value and return the product to A as the exit status. Will the program work with large numbers?

    


05. Name three advantages **waitpid** has over **wait**. Why can't a background process be terminated with the interrupt key?

    


06. Explain the difference in treatment meted out by the kernel to zombies and orphans.

    


07. Write a program that prompts for a command line to be executed and then uses an exec function to run it. The command line can contain shell meta-characters including redirection and piping symbols. (HINT: Take advantage of the shell's -c option.)

    


08. Write a program that runs the **ls -lids** command, but specifies a separate environment for the exec'd process. The new environment should have only the HOME and PATH variables. Prove that the MAIL and TERM variables are not available in the new process.

    


09. What are the structural changes that take place in memory when (i) a file is opened twice, (ii) its descriptor replicated.

    


10. Does each entry in the file descriptor table have a separate file table associated with it?

    


11. Look up the man page for any shell and understand the significance of the -c option. Next, write a program that prompts for a command, which is executed with **exec**, and **sh -c**. Try using the program with both external and internal (shell) commands. Does this program behave properly even when using wild-cards and pipes?

    


12. Invoke the command **vi foo &**, and explain why you can't input text to the editor.

    
