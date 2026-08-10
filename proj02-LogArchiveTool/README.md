# Log Archive Tool

A Bash tool that archives logs on a schedule by compressing them into a `tar.gz` file and storing them in a dedicated archive directory. This is useful for removing old logs and keeping the system clean while retaining the logs in a compressed format for future reference.

## Requirements

The tool runs from the command line, accepts a log directory, compresses the logs, and stores them in a new directory. The user can:

- Provide the log directory as an argument when running the tool.
- Compress the logs into a `tar.gz` file and store them in a new directory.
- Log the date and time of the archive to a file.

Example archive filename:

```
logs_archive_20240816_100648.tar.gz
```

## Files

| File          | Description                       |
| ------------- | --------------------------------- |
| `logarchive.sh` | The main interactive archive tool |
| `README.md`   | This documentation                |

## Usage

```bash
chmod +x logarchive.sh
./logarchive.sh
```

The script presents an interactive menu:

1. Specify log directory (default `/var/log`)
2. Specify number of days of logs to keep
3. Specify number of days of backup archives to keep
4. Run the log archiving process
5. Exit

When the archiving process runs, it:

- Creates an `archive` subdirectory.
- Finds logs older than the keep period and compresses them into a timestamped `tar.gz` file.
- Appends the archive date/time to `archive_log.txt`.
- Deletes the archived logs.
- Removes backup archives older than the retention period.

After the menu loop, the script asks whether to install a cron job for daily execution at `0 2 * * *`.
