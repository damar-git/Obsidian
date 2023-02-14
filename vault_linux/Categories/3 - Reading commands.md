
The following commands serve to perform reading operations on files.

***

## cat

Print a file content.

```bash
cat filename.txt
```

***

## tail

Print a specific number of lines starting from the bottom of the file (10 lines by default).

To set a specific number of lines you need to add the *-n* option.

```bash
tail filename.txt
tail -n 12 filename.txt
tail -12 filename.txt (shortened option)
```

A very useful option for the tail command is *-f* (it stands for follow).

Unlike the default behaviour which is to end after printing a certain number of lines, the *-f* option will follow the stream if new lines are added to the file.

A typical use case is reading a logfile while an application continues to add new contents.

```bash
> *tail -f logfile*
```

Press CTRL+c to exit the process.

***

## head

Complementary of *tail*, *head* command prints a specific number of lines starting from the top of the file. (10 lines by default)

Also for *head* to set a specific number of lines you need to add the *-n* option.

```bash
head filename.txt
head -n 3 filename.txt
head -3 filename.txt (shortened option)
```


***

## less

The *less* command not only allows to print a file content, but it brings a very useful interacting feature.

Once you send the command a reading session get started through which you can interact with the file lines, navigating or searching for a specific word.

```bash
less filename.txt
```

You can navigate the file content in many ways:

* *up* and *down* keys
* *space bar* and *b* to navigate page by page
* *G* to jump to the end of the file and *g* to jump back to the start

Search for a specific content:

* */word_to_search* to search forward
* *?word_to_search* to search backwards

Similiary to the option *-f* of the *tail* command, *less* command allows you to follow the file content stream by pressing the *F* key during the reading session. If new lines are added you get to ses the changes in real time.

To quit a follow session press *CTRL+c* while to quit the entire *less* session press *q*.

***

## grep

Search a file for lines containing a specific word.



```bash
grep word_to_search file.txt
grep -i word_to_search file.txt (Perform a case-insensitive search)
grep word_to_search file1.txt file2.txt (Perform a multiple file search)
grep -R word_to_search (Search all files in the current directory and in all of its subdirectories for a match**)
grep -v word_to_search file.txt (Search a file for non-matching lines)
grep -e regular_expression file.txt (Search a file for lines that match a regular expression)
```