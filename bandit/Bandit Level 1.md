# Bandit Level 0

## Objectives
Use SSH to connect to the OverTheWire Bandit server with the provided credentials and successfully log in as bandit0.

## Skills Used
- SSH
- Linux terminal navigation
- File reading from command line
- Basic remote server access

## Given Information
The username is bandit0 and the password is bandit0.

## Approach
Using a VM, I launched Kali Linux and opened a terminal. Through the terminal, I used SSH with the provided username, host, and port number

## Commands Used
`ssh bandit0@bandit.labs.overthewire.org -p 2220`
After logging in, I listed the files in the current directory:
`ls`
The output showed a file named readme.
To view the contents of the file, I used:
`cat readme`

## Explanation
The `ssh` command allows me to connect to the remote Bandit server. The `-p 2220` option specifies the port number since Bandit does not use the default SSH port.
The `ls` command lists files in the current directory, and the `cat` command prints the content of the file to the terminal.

## Result
The readme file contained the password for the next level
`Password: <REDACTED>`
## Security Takeaway
SSH is used for secure remote administration. Understanding how SSH works is important for both system administration and cybersecurity because misconfigured SSH access can become a major security risk.