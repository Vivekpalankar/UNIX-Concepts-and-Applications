## Notes

-   When running `cp -R <source_file> <destination_file>`, if the `<source_file>` designates a directory, **cp** copies the directory and the entire subtree connected at that point. If the `<source_file>` ends in a _/_, the contents of the directory are copied rather than the directory itself.

-   The `rm` utility removes symbolic links, not the files referenced by the links.

-   Line ending character used across different operating systems:  

        macOS/ UNIX     (LF)    (\n)  
        Classic Mac OS  (CR)    (\r)  
        Windows         (CRLF)  (\r\n)
