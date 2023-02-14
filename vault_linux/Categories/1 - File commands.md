
The following commands serve to perform operations on files.

***

## touch

Create an empty file. 

The touch command primary function is to modify a file timestamp but is commonly used for file creation. 
 
If the file already exists, this command will just update the modification date time, without effectively alter its content.

```bash
touch filename.txt
touch path/to/file filename.txt
```

***

## > (redirection)

Similiarly to *touch*, the **redirection** command creates an empty file.

**Be careful, this command will erase the file if it already exists, replacing it with an empty one without asking for confirmation!**

```bash
> filename.docx
> path/to/file filename.docx
```


Combined with some other commands output, this command allows to write that output to a file. Some examples:


```bash
ls > filename.txt (List the content of a specific directory and write it to a file)

cat file1.txt > file2.txt (**Read the content of file1.txt and write it to file2.txt)

grep word_to_search file.txt > result.txt (Search any line that contain a specific word in file.txt and write the output to result.txt)
```

***

## echo

*echo* command is used to display line of text/string that are passed as an argument.

```bash
echo some text
```

Combined with > command, *echo*  allows you to write text into a file. If the file does not exist it will be created. 

**Be careful as the content of an already existing file will be erased without asking for confirmation!**

```bash
echo "some text" > filename.txt
echo "some text" > path/to/file filename.txt
```

***
## cat

Combined with *>*, cat allows to write content into a file.

```bash
cat > filename.txt
```

After entered the command it will listen for the content input.

```bash
cat > filename.txt
hello
world!
```

The file will now contains the two lines we’ve entered. 

Press CTRL+d to terminate the command.

**If the file already has a content it will be overwritten so pay attention as this command does not ask for confirmation!**

To append the input to an existing file without erasing its original content, use **>>** operator.

```bash
cat >> filename
first line appendend
second line appended
```

***
## rm

Delete a file (rm stands for remove).

```bash
rm filename.txt
rm path/to/file filename.txt
```

It's also possible to remove all the files present in the directory at once. 

```bash
rm \* 
rm \path\to\files\* 
```

**Be careful as this command does not ask for confirmation!**

***

## cp

 Copy a file.

```bash
cp filename.txt destination_directory
```

Copy multiple file at once.

```bash
cp filename1.txt filename2.txt destination_directory
```

Copy all files present in a directory.

```bash
cp * destination_directory
cp source_directory/* destination_directory
```

By adding the -r option, if the destination_directory doesn't exist it will be created.

```bash
cp -r source_directory not_existing_directory
```

***

## mv

Move a file.

```bash
mv filename.txt destination_directory
mv path/to/file/filename.txt destination_directory
mv filename1.txt filename2.txt destination_directory
```

Move all file present in a directory at once.

```bash
mv \* destination_directory
mv source_directory/\* destination_directory
```

**If the file you want to move already exists in the target directory, the mv command will perform an override so pay attention because it will not ask for confirmation!**

***

## test

Check if a file exists.

```bash
test file.txt
```

Test command returns 0 / true as a successful exit status if the file exists, otherwise returns 1 / false.

It can be useful while chaining multiple commands:

```bash
test file.txt && echo "file.txt exists" && cp file.txt path/to/file
```
