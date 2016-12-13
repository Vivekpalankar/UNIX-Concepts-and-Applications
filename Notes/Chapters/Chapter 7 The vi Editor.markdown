## Notes

-   Press `[Ctrl-w]` to erase an entire word.
-   Press `[Ctrl-l]` in command mode to redraw screen.
-   Enter `/` in input mode. Then press `[Esc]` and enter `70a*[Esc]` to enter _*_ 70 times.
-   Press `[Ctrl-p]` for string completion. The matches are cycled. To cycle backwards press `[Ctrl-n]`.
-   10 ways to enter Input mode from command mode:  

        i     Insert text to left of cursor (existing text shifted right)
        a     Append text to right of cursor (existing text shifted right)
        I     Inserts text at beginning of line (existing test shifted right)
        A     Appends text at the end of line
        o     Opens line below
        O     Opens line above
        rch   Replaces single character under cursor with _ch_ (No [Esc] required)
        R     Replaces text from cursor to right (existing text overwritten)
        s     Replaces single character under cursor with any number of characters
        S     Replaces entire line (the line is cleared)
-   `ZZ`: Command mode command to save the buffer and quit the editor.
-   Vim suggests appending a **!** to an ex mode command every time it feels that you could be doing something that is potentially unsafe. **!** is the universal overriding operator.
-   To temporarily exit to UNIX shell, enter `:sh` in ex mode, `:!cmd` runs shell command _cmd_.
-   vim understands a word as a navigation unit. A word in Vim consists of a string of alphanumeric characters including underscore (_).
-   Word navigation keys:  

        b     move back to beginning of word
        e     move forward to end of word
        w     move forward to beginning of word
-   `B`, `E`, `W` perform the same function, except that punctuations are skipped.
-   _-_ character counts as a word in tcp-ip.
-   `0` or `|` moves to beginning of line, _30|_ moves to column 30.
-   Shortcuts for scrolling in Command mode:  

        [Ctrl-f]    Scroll forward
        [Ctrl-b]    Scroll backward
        [Ctrl-d]    Scroll half page forward
        [Ctrl-u]    Scroll half page backward
-   Command mode navigation commands:  

        40G     goes to line 40         (ex mode equivalent :40)
        1G      goes to first line      (ex mode equivalent command :1)
        G       goes to end of file     (ex mode equivalent command :$)
-   `x` is the text deletion command. The character under the cursor gets deleted, and the text on the right shifts left to fill up the space. If the cursor is at the end of line, next line is not pulled up, rather the characters to left are deleted.
-   The deletion of text towards left is handled by `X` command. Keep it pressed to delete all text to the beginning of the line.
-   `J` join the current line and the line following it.
-   The three commands, `/` (search), `n` (repeat search) and `.` (repeat last editing command), form a wonderful trio of search - search-repeat - edit-repeat commands. You'll often be tempted to use this trio in many situations where you want the same change to be carried out at a number of places. For instance, if you want to replace some occurrences of int with double, then first search for int with `/int`, change int to double with `3s`, repeat the search with `n`, and press `.` whenever you want the replacement to take place. To exclude embedded matched like printf, use regular expressions.
-   To startup vim by specifying a pattern, use the `+/` symbol before the pattern. E.g. To open file named _notes_ with the cursor station on the line containing the first occurrence of the word _UNIX_, enter: `vim +/UNIX notes` as command line.
-   The syntax for substitution in vim is `:s` (s comes after specifying the address part):  
        `:address/source_pattern/target_pattern/flags`  

    -   Address can be one or a pair of numbers separated by commas.

    -   The most common flag is `g` which carries out the substitution for all occurrences of pattern in a line.

    -   % can be used instead of 1,$ for address.

    -   If target pattern is left out, occurrences of source pattern are deleted.

    -   If `g` flag is left out, the substitution is carried out for the first occurrence in each addressed line.

    -   Add c in flag for interactive substitution `gc`
        -   `y` confirms substitution
        -   `n` deny substitution
        -   `q` aborts substitution
        -   `a` makes substitution non-interactive
