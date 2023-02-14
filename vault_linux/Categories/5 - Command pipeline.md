Command pipelines are a special kind of instructions chains, within which the output of a command is used as input of another command.

The command pipeline syntax is  **"command_1 | command_2 | command_3 | .... | command_N"**.

```bash
head -7 filename.txt | tail -5
```

	1 extract the first 7 lines of filename.txt starting from top
	2 print the last 5 lines starting from bottom

```bash
ls | head -3 | tail -1 > myoutput.txt
```

	 1 list the current directory content
	 2 extract the first 3 lines of the listed content
	 3 extract the last line and write the result to myoutput.txt 


```bash
ls -t | grep "data" | tail -1
```

	1 list the current directory content sorted by time
	2 extract the lines that contain the word "data"
	3 print the last line