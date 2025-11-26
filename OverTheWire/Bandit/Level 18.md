# Level 18

## Access for current level
Username: bandit18<br>
Password: x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO (acquired from previous level)<br>
SSH command: `ssh bandit18@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
The password for the next level is stored in a file readme in the home directory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

## Solution
If we try sshing as normal into bandit18 with the previous password, we don't actually get access (this was hinted at in the notes for the previous level). We're automatically logged out when trying to connect.

So instead we can use the ssh command like normal but just include some basic linux commands at the end of it. So if we want to see what files are in the home directory we can do `ssh bandit18@bandit.labs.overthewire.org -p 2220 ls -la`, this won't log us into the box but it will return a list of files on that box.

We can see a file called `readme` in there so now we can `cat` it with `ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme`

## Password for next level
cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8