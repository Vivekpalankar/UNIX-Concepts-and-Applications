## Notes

-   The currently running shells PID is stored in a special variable called `$` and can be evaluated using the command `echo $$`.

-   Built-in commands of shell don't create a separate process.

-   In `ps` output, the login shell can be easily identified by the presence of hyphen preceding the command name.

-   In most shells, a special variable called `!` stores the PID of the last background job and can be evaluated using the command `echo $!`.
