# tail

## Name

tail - output the last part of files

## Synopsis

tail [OPTION]... [FILE]...

## Description

The `tail` command prints the last 10 lines of each FILE to standard output. If no FILE is specified, or if FILE is "-", `tail` reads from standard input.

## Options

- `-n, --lines=[+]NUM`: output the last NUM lines, instead of the last 10; or use -n +NUM to output starting with line NUM
- `-c, --bytes=[+]NUM`: output the last NUM bytes; or use -c +NUM to output starting with byte NUM
- `-f, --follow[={name|descriptor}]`: output appended data as the file grows; an absent option argument means 'descriptor'
- `--pid=PID`: with -f, terminate after process ID, PID dies
- `-q, --quiet, --silent`: never output headers giving file names
- `-s, --sleep-interval=S`: with -f, sleep for approximately S seconds (default 1.0) between iterations; with inotify and --pid=P, check process P at least once every S seconds
- `-v, --verbose`: always output headers giving file names
- `--help`: display this help and exit
- `--version`: output version information and exit

## Cheat Sheet

| Option | Description |
|--------|-------------|
| -n, --lines=[+]NUM | Output the last NUM lines, instead of the last 10; or use -n +NUM to output starting with line NUM |
| -c, --bytes=[+]NUM | Output the last NUM bytes; or use -c +NUM to output starting with byte NUM |
| -f, --follow[={name\|descriptor}] | Output appended data as the file grows; an absent option argument means 'descriptor' |
| --pid=PID | With -f, terminate after process ID, PID dies |
| -q, --quiet, --silent | Never output headers giving file names |
| -s, --sleep-interval=S | With -f, sleep for approximately S seconds (default 1.0) between iterations; with inotify and --pid=P, check process P at least once every S seconds |
| -v, --verbose | Always output headers giving file names |
| --help | Display this help and exit |
| --version | Output version information and exit |

## Examples

1. Display the last 10 lines of a file:
```
tail file.txt
```

2. Display the last 20 lines of a file:
```
tail -n 20 file.txt
```

3. Display the last 100 bytes of a file:
```
tail -c 100 file.txt
```

4. Follow the growth of a log file and display new lines as they are appended:
```
tail -f log.txt
```

## Tips & Tricks

- Use the `-f` option to continuously monitor a log file and display new lines as they are appended.
- Combine the `-n` and `-f` options to monitor the last N lines of a log file in real-time.
- Use the `-c` option to display the last N bytes of a file, which can be useful for examining binary files.
- To suppress the headers giving file names, use the `-q` option.
- Increase the sleep interval using the `-s` option to reduce the frequency of checking for new lines when using `-f`.
- Use the `--pid` option to terminate `tail` after a specific process ID dies.
- The `-v` option can be used to always display headers giving file names, even when only one file is being monitored.
- Refer to the manual page for more advanced usage and options.

**Note:** The `tail` command is commonly used for log file analysis and monitoring. It is a versatile tool for observing changes in files and extracting relevant information from the end of files.