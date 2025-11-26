# Level 5

## Access for current level
Username: bandit5<br>
Password: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw (acquired from previous level)<br>
SSH command: `ssh bandit5@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

## Solution
Loads of files in separate directories inside of `/inhere`. We are told the password file is 1033 bytes in size, is human-readable, and is not executable. We can use `find .` inside `/inhere` to give us a list of every file within the directory. Then we can use the `-size` flag to specify the size of the file we want. `find . -size 1033c` (the c is for bytes). File is in `maybehere07/.file2`

## Password for next level
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG