
The following commands serve to perform operations on directories.

***

## ls

List the content of a specific directory.

```bash
ls (list the content of the current working directory)
ls path/to/directory (list the contet of the given path)
ls ..* (list the content of the parent directory)
ls -d */ (list only directories)
ls * (list the contents of the directory with its subdirectories)
ls -R* (list directories and their content recursively, down to the last file)
ls -t (sort by time, newest to oldest)
```

***

## cd

Move from a directory to another one (cd stands for change directory).

```bash
cd directoryname
cd directory/subdirectory
```

Using the **..** sign you can indicate the parent directory and move backward.

```bash
cd ..  (one step back)
cd ../.. (two consecutives steps back)
cd ../another_directory (step back and move to another_directory)
```

***

## mkdir

Create an empty directory.

```bash
mkdir directory_name
```

To create nested directories you need to add the -p option.

```bash
mkdir -p directory/subdirectory
```

***

## rmdir

Remove a directory (must be empty). 

```bash
rmdir directory_name
```

You can also remove multiple directories at once:

```bash
rmdir first_directory second_directory
```

To delete a directory that contains files (and eventually other directories) you need to use the **rm** command add the -rf option. **Be careful as this command does not ask for confirmation!**

```bash
rm -rf directoryname
```

***

## mv

Move a directory.

```bash
mv directory_name target_directory
```

If the target directory already contains a directory with the same name as the one you want to move, the operation will not be performed.

***

## cp

Copy a directory.

Even if the source directory is not empty, you must add the -r option to the **cp** command to perform this operation.

```bash
cp -r source_directory target_directory
```

If the target directory already contains a directory with the same name as the one you want to move, the operation will merge the two contents. 

**Be careful as if the already existing directory contains a file with the same name as one present inside the directory you want to copy, that file will be overwritten and its original content will be lost!**

