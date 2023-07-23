
# `head`

## Name
**head** - Output the first part of files

## Synopsis
The `head` command is used in the format `head [OPTION]... [FILE]...`. This command will output the first part of the files given to it as input.

## Description
The `head` command in Linux is used to print the top N number of data of the given input. By default, it prints the first 10 lines of the specified files. If more than one file name is provided then data from each file is preceded by its file name.

## Options
Here are the options for the `head` command, with the most popular options listed first:

- `-n, --lines=[-]K`: Print the first K lines instead of the first 10; with the leading '-', print all but the last K lines of each file. 

- `-c, --bytes=[-]K`: Print the first K bytes of each file; with the leading '-', print all but the last K bytes of each file.

- `-q, --quiet, --silent`: Never print headers giving file names.

- `-v, --verbose`: Always print headers giving file names.

- `--help`: Display a help message and exit.

- `--version`: Output version information and exit.

## Cheat Sheet

| Option | Description |
| --- | --- |
| `-n, --lines=[-]K` | Print the first K lines |
| `-c, --bytes=[-]K` | Print the first K bytes |
| `-q, --quiet, --silent` | Never print headers giving file names |
| `-v, --verbose` | Always print headers giving file names |
| `--help` | Display a help message and exit |
| `--version` | Output version information and exit |

## Examples

**Example 1:**

The `-c` option is a little more complex as it deals with bytes. Here's an example of its usage:

```bash
head -c 20 myfile.txt
```

This command will output the first 20 bytes of myfile.txt. Remember, a byte is a unit of digital information that most commonly consists of eight bits. 

## Tips & Tricks

- Remember that if you want to view the top 'n' number of lines you can use `-n` option. For example, `head -n 20 myfile.txt` will display the first 20 lines of myfile.txt.

- If you want to view the beginning of several files you can include several file names in the command. For example, `head myfile1.txt myfile2.txt` will show the beginning of both myfile1.txt and myfile2.txt.

- If you use `head` with no file name it will read from standard input. For example, `ls -l | head` will output the first 10 lines of the directory listing.

- If you want to view all but the last 'n' lines or bytes of a file, you can use `-n` or `-c` with a leading '-'. For example, `head -n -5 myfile.txt` will output all the lines of myfile.txt except for the last 5.

- Always remember that `head`, like most Linux commands, is case sensitive. Be sure to enter all commands exactly as shown.

Please note that these are general tips and tricks and may not apply to all distributions of Linux. Always check the man pages on your specific distribution for the most accurate information.
