# tail

## Name
tail - output the last part of files

## Synopsis
tail [OPTION]... [FILE]...

## Description
The `tail` command displays the last part of one or more files. By default, it prints the last 10 lines of each specified file to the standard output.

## Options
- `-n, --lines=[+]NUM`: Output the last NUM lines instead of the last 10. If NUM is prefixed with a '+', it outputs starting with the line NUM.
- `-c, --bytes=[+]NUM`: Output the last NUM bytes instead of the last 10 bytes. If NUM is prefixed with a '+', it outputs starting with the byte NUM.
- `-f, --follow[={name|descriptor}]`: Output appended data as the file grows. The -f option is ignored if the standard input is a pipe, but not if it is a FIFO.
- `-F`: Same as --follow=name --retry.
- `--pid=PID`: With -f, terminate after process ID, PID, dies.
- `--max-unchanged-stats=N`: With --follow=name, reopen a FILE which has not changed size after N (default 5) iterations to see if it has been unlinked or renamed (this is the usual case of rotated log files). With inotify, this option is rarely useful.
- `-q, --quiet, --silent`: Never output headers giving file names.
- `-s, --sleep-interval=N`: With -f, sleep for approximately N seconds (default 1.0) between iterations. With inotify and --pid=P, check process P at least once every N seconds.
- `-v, --verbose`: Always output headers giving file names.
- `--help`: Display this help and exit.
- `--version`: Output version information and exit.

## Cheat Sheet

| Option | Description |
| ------ | ----------- |
| -n, --lines=[+]NUM | Output the last NUM lines instead of the last 10. If NUM is prefixed with a '+', it outputs starting with the line NUM. |
| -c, --bytes=[+]NUM | Output the last NUM bytes instead of the last 10 bytes. If NUM is prefixed with a '+', it outputs starting with the byte NUM. |
| -f, --follow[={name\|descriptor}] | Output appended data as the file grows. The -f option is ignored if the standard input is a pipe, but not if it is a FIFO. |
| -F | Same as --follow=name --retry. |
| --pid=PID | With -f, terminate after process ID, PID, dies. |
| --max-unchanged-stats=N | With --follow=name, reopen a FILE which has not changed size after N (default 5) iterations to see if it has been unlinked or renamed (this is the usual case of rotated log files). With inotify, this option is rarely useful. |
| -q, --quiet, --silent | Never output headers giving file names. |
| -s, --sleep-interval=N | With -f, sleep for approximately N seconds (default 1.0) between iterations. With inotify and --pid=P, check process P at least once every N seconds. |
| -v, --verbose | Always output headers giving file names. |
| --help | Display this help and exit. |
| --version | Output version information and exit. |

## Examples
1. Display the last 10 lines of a file:
```
tail file.txt
```

2. Display the last 5 lines of a file:
```
tail -n 5 file.txt
```

3. Output the last 100 bytes of a file:
```
tail -c 100 file.txt
```

## Tips & Tricks
- Use the `-f` option to continuously monitor a file for changes and display new lines as they are appended.
- Combine the `-f` and `-n` options to monitor the last N lines of a file in real-time.
- Use the `--max-unchanged-stats` option to handle rotated log files that may have been unlinked or renamed.
- Suppress the headers giving file names with the `-q` option for cleaner output.
- Increase the sleep interval between iterations with the `-s` option to reduce resource usage.
- Always include the `-v` option to display headers giving file names for better context.
- Use the `--help` option to quickly refer to the command's options and their descriptions.
- Check the version of `tail` with the `--version` option.

Now you have a user-friendly and easy-to-read manual page for the `tail` command.