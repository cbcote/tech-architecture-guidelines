# Powershell Cheat Sheet

## Table of Contents

- [Commands](#Commands)
- [Operators](#operators)
- [Variables](#variables)
- [Arrays](#arrays)
- [Hash Tables](#hash-tables)
- [Functions](#functions)
- [Loops](#loops)
- [Conditions](#conditions)
- [Error Handling](#error-handling)
- [Modules](#modules)
- [Files](#files)
- [Processes](#processes)
- [Networking](#networking)
- [Services](#services)
- [Security](#security)

## Commands

| Command             | Example                                       | Description                                                             | Flags/Options                   | Output Example                    | Common Use Cases                                 | Alternative Commands     |
|---------------------|-----------------------------------------------|-------------------------------------------------------------------------|----------------------------------|-----------------------------------|-------------------------------------------------|--------------------------|
| `Get-ChildItem`      | `Get-ChildItem -Force`                        | Lists files and directories in the current directory                    | `-Force` (hidden), `-Recurse`    | Detailed file listing              | Checking contents of a directory                 | `dir`, `ls`              |
| `Set-Location`       | `Set-Location C:\Path\To\Directory`           | Changes the current directory                                           | N/A                              | Changes prompt to new directory   | Navigating between directories                   | `cd`, `chdir`            |
| `Get-Location`       | `Get-Location`                                | Prints the current working directory                                    | N/A                              | Shows current directory path      | Verifying the current directory                  | `pwd`                    |
| `Copy-Item`          | `Copy-Item file1.txt C:\Path\To\Destination`  | Copies a file or directory                                              | `-Recurse`, `-Force`             | No output, unless error           | Copying files or directories                     | `cp`                     |
| `Move-Item`          | `Move-Item file1.txt C:\Path\To\Destination`  | Moves a file or renames it                                              | `-Force`, `-Confirm`             | No output, unless error           | Renaming or moving files                         | `mv`, `rename`           |
| `Remove-Item`        | `Remove-Item file1.txt`                       | Removes a file or directory                                             | `-Recurse`, `-Force`             | No output, unless error           | Deleting files or directories                    | `rm`                     |
| `New-Item`           | `New-Item -Name new_directory -ItemType Directory` | Creates a new file or directory                                         | `-ItemType`, `-Force`            | No output, unless error           | Creating new directories or files               | `mkdir`, `touch`         |
| `Get-Content`        | `Get-Content file.txt`                        | Displays the contents of a file                                         | `-Tail`, `-TotalCount`           | Displays file contents            | Viewing or concatenating file contents           | `cat`, `less`, `more`    |
| `Select-String`      | `Select-String -Pattern 'pattern' file.txt`   | Searches for a pattern in a file                                        | `-CaseSensitive`, `-AllMatches`  | Matching lines from file          | Finding specific information in logs or files    | `grep`, `findstr`        |
| `Get-Process`        | `Get-Process`                                 | Displays currently running processes                                    | `-Name`, `-Id`, `-FileVersionInfo`| List of running processes         | Monitoring system resource usage and processes   | `ps`, `top`, `htop`      |
| `Stop-Process`       | `Stop-Process -Id 1234`                       | Kills a process by its process ID                                       | `-Force`                         | No output, unless error           | Terminating processes                             | `kill`, `pkill`, `taskkill`|
| `Get-Help`           | `Get-Help Get-Process`                        | Displays the help documentation for a command                           | `-Full`, `-Examples`             | Manual page                      | Looking up detailed command information          | `man`, `help`            |
| `Start-Job`          | `Start-Job -ScriptBlock {Get-Process}`        | Starts a background job                                                 | `-Name`, `-Credential`           | Job object ID                     | Running processes in the background              | `nohup`, `bg`            |
| `Get-Service`        | `Get-Service`                                 | Displays the status of services                                         | `-Name`, `-Status`               | List of services                  | Monitoring services running on the system        | `service --status-all`   |
| `Start-Service`      | `Start-Service -Name ServiceName`             | Starts a service                                                        | `-DisplayName`                   | No output, unless error           | Starting a stopped service                       | `systemctl start`, `service` |
| `Stop-Service`       | `Stop-Service -Name ServiceName`              | Stops a service                                                         | `-DisplayName`, `-Force`         | No output, unless error           | Stopping a running service                       | `systemctl stop`, `service` |
| `Restart-Computer`   | `Restart-Computer -Force`                     | Restarts the computer                                                   | `-Force`, `-Wait`                | No output, unless error           | Restarting the system                            | `shutdown -r`, `reboot`  |
| `Test-Connection`    | `Test-Connection google.com`                  | Sends ICMP echo requests to a host (ping)                               | `-Count`, `-TTL`                 | ICMP response summary             | Testing network connectivity                     | `ping`, `tracert`        |
| `Invoke-WebRequest`  | `Invoke-WebRequest https://example.com`        | Transfers data from or to a server using various protocols (HTTP, HTTPS)| `-OutFile`, `-UseBasicParsing`   | HTML or other output              | Downloading files or interacting with web APIs   | `curl`, `wget`           |
| `Write-Output`       | `Write-Output "Hello World"`                  | Outputs text or objects to the console                                  | N/A                              | Printed text                     | Outputting text or variables                     | `echo`, `print`          |
| `Get-History`        | `Get-History`                                 | Displays the list of previously used commands                           | `-Id`, `-Count`                  | Command history                   | Reviewing or repeating past commands             | `history`, `fc`          |
| `Set-Alias`          | `Set-Alias ll Get-ChildItem`                  | Creates a shortcut for a cmdlet or command                              | `-Description`, `-Force`         | No output, unless error           | Creating custom command aliases                 | `alias`                 |
| `Invoke-Command`     | `Invoke-Command -ScriptBlock {Get-Process}`   | Runs commands locally or remotely                                      | `-ComputerName`, `-Credential`   | Output of command                 | Executing remote or local scripts                | `ssh`, `plink`           |
| `Get-Date`           | `Get-Date -Format "yyyy-MM-dd"`               | Displays the current date and time                                      | `-UFormat`, `-DisplayHint`       | Current date and time             | Checking or formatting the system date and time  | `date`                  |
| `Measure-Object`     | `Measure-Object -Property Length -Sum`        | Measures properties of objects, such as length or count                 | `-Average`, `-Sum`, `-Minimum`   | Sum, count, average, etc.         | Summing values, counting lines/files, etc.       | `wc`, `sum`              |



## Operators

| Operator   | Description                                                  | Example                           | Use Case                                                                 |
|------------|--------------------------------------------------------------|-----------------------------------|-------------------------------------------------------------------------|
| `>`        | Redirects output to a file (overwrites the file)             | `Get-Process > output.txt`        | Write the output of `Get-Process` to a file, overwriting the content     |
| `>>`       | Redirects output to a file (appends to the file)             | `Get-Process >> output.txt`       | Append the output of `Get-Process` to the file without overwriting       |
| `2>`       | Redirects error output (stderr) to a file                    | `Get-Process -Invalid 2> error.txt`| Write error messages to a file                                          |
| `2>>`      | Appends error output (stderr) to a file                      | `Get-Process -Invalid 2>> error.txt`| Append error messages to a file without overwriting                    |
| `*>`       | Redirects both output (stdout) and error (stderr) to a file  | `Get-Process *> output.txt`       | Write both standard output and error messages to a file                 |
| `*>>`      | Appends both output (stdout) and error (stderr) to a file    | `Get-Process *>> output.txt`      | Append both standard output and error messages to a file without overwriting |
| `|`        | Pipe: Sends output from one command as input to another      | `Get-Process | Where-Object {$_.CPU -gt 100}` | Pass the output of `Get-Process` to `Where-Object` for filtering        |
| `|&`       | Pipe both stdout and stderr to another command               | `Get-Process |& Where-Object {$_ -gt 100}` | Send both output and errors to the next command for processing          |
| `Out-Null` | Discards the output                                          | `Get-Process | Out-Null`            | Discard the output of a command (similar to redirecting to `/dev/null`) |
| `Out-File` | Sends output to a file                                       | `Get-Process | Out-File output.txt`  | Write output to a file using the `Out-File` cmdlet                      |
| `Out-Host` | Sends output to the console                                  | `Get-Process | Out-Host`            | Display output in the terminal                                          |
| `Out-String` | Converts output to a string                                | `Get-Process | Out-String`          | Convert command output to a string                                      |
| `Tee-Object` | Sends output to both a file and the console                | `Get-Process | Tee-Object output.txt` | Save output to a file and display it in the terminal simultaneously     |
| `Read-Host` | Prompts the user for input                                  | `$input = Read-Host "Enter value"`| Read user input from the terminal                                       |

### Notes:
- **Standard Output (stdout)**: The output stream for the results of commands.
- **Standard Error (stderr)**: The stream for error messages.
- **Pipelines (`|`)**: PowerShell pipes data as objects, making it more powerful for object manipulation compared to traditional text-based shells.

