Linux allows to use system built-in text editors for writing and editing files in plain text.

***

## vi

Vi is a built-in modal text editor that meets all the needs for working on files content.

```bash
vi file.txt
```

The above command will start a modal window. 

The Vi editor has two modes, Command and Insert. 

When you first open a file with Vi, you are in Command mode. Command mode means you can use keyboard keys to navigate, delete, copy, paste, and other tasks, except entering text.

To start Insert mode press **i**.

**Before start editing a file it's highly recommended to create a backup of that file.**

In Insert mode you can enter text, use the **Enter** key to go to a new line, use the arrow keys to navigate text. 

To return to Command mode, press the **Esc** key once.

Once back to Command mode you can save or quit the modal window.

```bash
:w -> Save and continue editing.
:w name.txt -> Save to a new file name.txt.
:wq -> Save and quit/exit vi.
:q! -> Quit vi without save changes.
x -> Delete single character.
dd -> Delete entire line.
gg -> Go to first line in a file.
yy -> Copy a line of text.
p -> Paste a copied line below the current line.
```

