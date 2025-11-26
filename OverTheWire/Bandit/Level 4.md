# Level 4

## Access for current level
Username: bandit4<br>
Password: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ (acquired from previous level)<br>
SSH command: `ssh bandit4@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

## Solution
10 files found in `/inhere` directory. Could just look through them all, or use `strings` to print out all the readable strings in every file (need to specify the path though) -> `strings ~/inhere/*`

## Password for next level
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw