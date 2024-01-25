
# Shell Scripting

- **Automation:** Simplifying and streamlining repetitive tasks.

## Basic Commands

- **Create a File:**
  - Use `touch <fileName>` to create a new file.

- **List Files:**
  - `ls`: Lists files in the current directory.
  - `ls -ltr`: Lists files in long format with timestamps, sorted by modification time.

- **Manual:**
  - Use `man <command>` for manual pages and information about commands.

- **Edit or Write a File:**
  - `vi <fileName>` or `vim <fileName>`: Open a file for editing.

## Scripting Basics
- **Shebang Line:**
  - `#!/bin/bash`: Specifies the executable for the script.
  - `#!/bin/sh`: Links to `#!/bin/dash`.

## Working with Files
- **Printing:**
  - Use `echo "statement"` to print text.

- **Write in a File:**
  - Open a file using `vi` or `vim`.
  - Press `I` to enter insert mode and write content.

- **Saving a File:**
  - Press `Esc`.
  - Type `:wq` to save and quit.

- **Quitting a File:**
  - Press `Esc`.
  - Type `q` to quit.

- **View Contents of a File:**
  - Use `cat <fileName>` to display the file's content.

- **Execute a File:**
  - Run scripts using `sh <fileName>` or `./<fileName>`.

## Permissions and Execution
- **Change Mode (chmod):**
  - Use `chmod [permissions] <fileName>` to change file permissions.

  | Octal Number | Permission          | Symbolic Representation |
  |--------------|---------------------|-------------------------|
  | 0            | No permission       | `---`                   |
  | 1            | Execute             | `--x`                   |
  | 2            | Write               | `-w-`                   |
  | 3            | Write + Execute     | `-wx`                  |
  | 4            | Read                | `r--`                   |
  | 5            | Read + Execute      | `r-x`                  |
  | 6            | Read + Write        | `rw-`                  |
  | 7            | Read + Write + Execute | `rwx`                |

## File System Navigation
- **Checking Present Directory:**
  - Use `pwd` to see the present working directory.

- **Create Folder:**
  - Use `mkdir <folderName>` to create a new folder.

- **Change Directory:**
  - Use `cd <path>` to change into a directory.
  - Use `cd ..` to go back to the previous directory.

## System Information
- **List CPU:**
  - Use `nproc` to display the number of available processing units.

- **List Memory:**
  - Use `free` to view information about available memory.

- **List Both:**
  - Use `top` to display dynamic real-time information about system resources.

## Checking Disk Space:
- `df`: Displays disk space usage.
- `df -hT`: Displays disk space usage in a human-readable format with filesystem type.

## Script Execution and Debugging:
- Run script in debug mode: `set -x`
- Exit when an error occurs: `set -e`
- Exit in case of pipe fail: `set -o pipefail`

## Listing Processes:
- `ps -ef`: Lists out all processes.

## Integration of Commands:
- Pipe (`|`): Connects the output of one command to the input of another.
  Example: `ps -ef | grep <selector>`

## Selecting Particular Output:
- `ps -ef | grep <selector> | awk -F " " '{print $<colNumber>}'`

## Internet Requests:
- `curl -X GET <url>`
- `curl -s <fileUrl>`: Retrieves the content silently.

## File Download:
- `wget <url>`

## Finding Files:
- `find / -name <fileName>`: Searches for a file in the specified directory.

## Switching to Root User:
- `sudo su -`: Combines `sudo` (granting root privileges), `su` (switch user), and `-` (switch to root user).

## Conditional Statements:
### If-Else Example:
```bash
a=4
b=10

if [ $a -gt $b ]; then
    echo "a is greater than b"
else
    echo "b is greater than a"
fi
```

Certainly! Here's the Markdown file containing the updated notes with additional curl commands:

markdown
Copy code
# Shell Scripting - Additional Notes

## Checking Disk Space:
- `df`: Displays disk space usage.
- `df -hT`: Displays disk space usage in a human-readable format with filesystem type.

## Script Execution and Debugging:
- Run script in debug mode: `set -x`
- Exit when an error occurs: `set -e`
- Exit in case of pipe fail: `set -o pipefail`

## Listing Processes:
- `ps -ef`: Lists out all processes.

## Integration of Commands:
- Pipe (`|`): Connects the output of one command to the input of another.
  Example: `ps -ef | grep <selector>`

## Selecting Particular Output:
- `ps -ef | grep <selector> | awk -F " " '{print $<colNumber>}'`

## Internet Requests:
- `curl -X GET <url>`
- `curl -s <fileUrl>`: Retrieves the content silently.

## File Download:
- `wget <url>`

## Finding Files:
- `find / -name <fileName>`: Searches for a file in the specified directory.

## Switching to Root User:
- `sudo su -`: Combines `sudo` (granting root privileges), `su` (switch user), and `-` (switch to root user).

## Conditional Statements:
### If-Else Example:
```bash
a=4
b=10

if [ $a -gt $b ]; then
    echo "a is greater than b"
else
    echo "b is greater than a"
fi
```

### For Loop Example:
```bash
for i in {1..10}; do
    echo $i;
done
```
## Process Management:

- **Killing a Process:** `kill -9 <processId>`

## Trapping Signals:

- **Trap Interrupt Signal (SIGINT):** `trap "echo 'message'" SIGINT`

## Additional Curl Commands:

| Purpose                                     | Command                                              |
|---------------------------------------------|------------------------------------------------------|
| Fetch raw content of a file from GitHub      | `curl -s https://raw.githubusercontent.com/user/repo/branch/file` |
| Download a file and save with the original name | `curl -LOJ https://raw.githubusercontent.com/user/repo/branch/file` |
| Make a GET request to a URL                  | `curl -s https://example.com`                        |
| Make a POST request with data                | `curl -X POST -d "key1=value1&key2=value2" https://example.com` |
| Set custom headers in a request              | `curl -H "HeaderName: HeaderValue" https://example.com` |
| Follow redirects and download                | `curl -LOJ https://example.com/redirected-url`      |
| Download multiple files sequentially         | `curl -O file1.txt -O file2.txt https://example.com`|
| Specify a user agent in the request          | `curl -A "User-Agent String" https://example.com`    |
| Send a request with basic authentication    | `curl -u username:password https://example.com`      |
| Print information about the request/response | `curl -v https://example.com`                        |

