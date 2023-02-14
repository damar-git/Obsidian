Chaining commands in Linux allows to execute multiple commands at the same time, by eventually applying logical operators.


***

## ; (semi-colon)

The command following this operator will execute even if the command preceding this operator is not successfully executed.

Since the failure of a command doesn't stop the execution, the chain behaviour could be unexpected.

```bash
touch file.txt ; echo "text" > file.txt ; rm file.txt
```

***

## && (AND)

The command following this operator will only execute if the command preceding this operator has been successfully executed.

```bash
rm file.txt && touch file.txt && cp file.txt destination/folder
```


***

## || (OR)

The command succeeding this operator is only executed if the command preceding it has failed. 

It works as an if-else statement.

```bash
mv file.txt destination_folder || touch file.txt destination_folder
```

***

In Bash, operators with the same precedence are left-associative. That is, in the absence of grouping structures, leftmost operations are executed first.

```bash
cat file.txt || touch file.txt && cat file.txt
```

if `cat file.txt` is executed succesfully, the `||` operator short-circuits and the whole statement is considered true without the need to evaluate `touch file.txt` as you would expect. 

Now it remains to do the rightmost operation, `cat file.txt`. 

Since the first operation evaluated to true, it's as if we are executing:

```bash
cat file.txt && cat file.txt
```

Commands may also be grouped:

```bash
(test file.txt || test file2.txt) && touch file3.txt 
```

If either file.txt or file2.txt exist than file3.txt will be created.