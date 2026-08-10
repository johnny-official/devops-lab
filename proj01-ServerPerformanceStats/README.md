# Server Performance Stats

A Bash script that analyses basic server performance statistics. It prints a report of uptime, CPU, memory, disk usage, and the top processes by memory and CPU usage.

## Requirements

The script can run on any Linux server and reports:

- Total CPU usage
- Total memory usage (free vs used, including percentage)
- Total disk usage (free vs used, including percentage)
- Top 5 processes by CPU usage
- Top 5 processes by memory usage

## Files

| File              | Description                          |
| ----------------- | ------------------------------------ |
| `server-stats.sh` | The main analysis script             |
| `README.md`       | This documentation                  |

## Usage

```bash
chmod +x server-stats.sh
./server-stats.sh
```

## Output

- **System uptime** — how long the server has been running plus load averages.
- **CPU usage** — computed as `100 - idle` (top reports the idle percentage).
- **Memory usage** — totals and percentages from `free`, converted from KB to GiB.
- **Disk usage** — root filesystem usage, accounting for reserved space.
- **Top 5 processes** — sorted by memory and by CPU, showing user, PID, percentage, and command.
