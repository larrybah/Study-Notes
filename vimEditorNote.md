# Notes on how to work with vim (Basics)

Opening vim files type: vim or vi and the files name. eg `vim file.txt` or `vi file.c`

## Editing Files

After opening the file press escape key `esc` and press colon `:` then  `i` to go into insert mode, here you can type all you want.

After typing all you need you press `esc` and then press `w` to write it to file, and the press `q` to exit. 

> You can also use `wq` to write and save the file all together. 
>
> And you can use capital `ZZ` to write and save the file without typing colon.
>
> To delete a previously typed character press lowercase `s`.
>
> To *undo* you press Capital `C` and to *redo* press lowercase `u`.
>
> And to delete and entire line or sentence press uppercase `S`.

## Navigation

> To move to the end of a line you press the dolar sign `$` and to move to the start press `o`.
> 
> On Your keyboard keys use the **`Home`** to go to start of the line, use your **`End`**
> 
> To copy press double `yy` and to paste press `p`
> 
> To go the first line of your document use double `gg`.
> 
> To move to paticular number line press colon then number `:10`.

## Line Numbers

> setting line Numbers in a document press `esc` and then colon `:` and then `setnumber` like so **`:setnumber`**
>
> To deactivate line numbers **`:setnonumber`**.
>
