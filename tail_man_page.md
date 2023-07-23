
# **Command**
## `tail`

---

## **Name**
tail - output the last part of files

---

## **Synopsis**
`tail` [OPTION]... [FILE]...

---

## **Description**
`tail` prints the last 10 lines of each FILE to standard output. With more than one FILE, it precedes each set of output with a header giving the file name. With no FILE, or when FILE is -, it reads from standard input.

---

## **Options**

*Most Popular Options:*

- `-f` : Follow. This option outputs appended data as the file grows.
- `-n` : Number. Use `-n` followed by `NUMBER` to output the last NUMBER lines, instead of the last 10.
- `--pid=PID` : Terminate after process ID, PID dies.

*All Other Options:*

- `-c` : The `-c` option is like `-n` but counts the bytes instead of lines.
- `-q` : Never output headers giving file names.
- `-s` : Sleep for approximately `NUMBER` seconds between iterations.
- `-v` : Always output headers giving file names.
- `-z` : Line delimiter is NUL, not newline.

---

## **Cheat Sheet**

| Option | Description |
|--------|-------------|
| -f     | Follow appended data as the file grows. |
| -n     | Output the last NUMBER lines, instead of the last 10. |
| --pid  | Terminate after process ID, PID dies. |
| -c     | Counts the bytes instead of lines. |
| -q     | Never output headers giving file names. |
| -s     | Sleep for approximately NUMBER seconds between iterations. |
| -v     | Always output headers giving file names. |
| -z     | Line delimiter is NUL, not newline. |

---

## **Examples**

1. Following a Log File:
\```bash
tail -f /var/log/syslog
\```
This command will keep the file open and show any new lines that are added to the end. This is especially useful with log files, which append new entries to the end.

2. Displaying a Certain Number of Lines:
\```bash
tail -n 20 /var/log/syslog
\```
This command will display the last 20 lines of the file.

---

## **Tips & Tricks**

- Using `tail` with `-f` option can be a lifesaver when you're trying to troubleshoot an issue that's happening right now. You can see log entries in real time as they're being written.

- To view the content of two or more files use the following syntax:
\```bash
tail file1 file2 file3
\```

- The `tail -n` option can be used to show any number of final lines from the file. For example, `tail -n 5` would show the last five lines.

- `tail` and `head` can be used together to get a section of a file. For example, to get lines 15 through 20 of a file, you might `head -20 file | tail -6`.

- You can also `tail` the output of a command by piping the command into `tail`. For example, `dmesg | tail` would show the last ten lines of the system message buffer.

- Be aware that using the `-f` option will keep the command running until you stop it with Ctrl+C.
