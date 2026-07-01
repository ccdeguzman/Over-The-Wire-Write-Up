# Bandit Level 1 → 2 

## Objectives
Use the password in the `readme` file from bandit level 1 → 2 to log into bandit1 through SSH on port 2220

## Skills Used
- SSH
- Linux terminal navigation
- File reading from command line
- Basic remote server access
- Handling special filenames

## Given Information
The file is in the home directory called `-`

## Approach
Through the terminal, connect to the server using SSH with bandit1 account and the password obtained from the previous level.
`ssh bandit1@bandit.labs.overthewire.org -p 2220`
After logging in, I listed the files in the home directory using command:
`ls`
The output shows a file called `-`
The `-` character causes confusion because many commands treat it as a special character. To clearly tell the shell that I wanted to read the file called `-`, I ran the command:
`cat ./-`

## Explanation
The `./` means current directory. The `cat ./-` command tells Linux to read the file literally called `-`.
The `cat` command is used to print the contents of a file in the terminal.

## Result
The readme file contained the password for the next level
`Password: <REDACTED>`

## What I learned
This level taught me that depending on the name of the file, it can cause conflict with how Linux commands interpret arguments. I learned that using a relative path `./file_name` can help safely reference files with unusual names.

## Security Takeaway
Unusual filenames can cause confusion during file analysis, scripting, or incident response, so it is important to use precise file paths while working in the terminal. 