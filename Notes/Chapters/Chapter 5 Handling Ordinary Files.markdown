## Notes

-   When running `cp -R source destination`, if `source` designates a directory then **cp** copies the directory and the entire subtree connected at that point. If `source` ends with a `/`, the contents of the directory are copied rather than the directory itself.

-   The `rm` utility removes the symbolic link if used with one and not the files referenced by it.

-   Line ending character used across different operating systems:

        macOS/UNIX      (LF)    (\n)  
        Classic Mac OS  (CR)    (\r)  
        Windows         (CRLF)  (\r\n)
