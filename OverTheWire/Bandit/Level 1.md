# Level 1

## Access for current level
Username: bandit1<br>
Password: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If (acquired from previous level)<br>
SSH command: `ssh bandit1@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
The password for the next level is stored in a file called - located in the home directory.

## Solution
Home directory contained file called `-`. Can't cat this as its a special character. Have to specify the path to the file `cat ./-` for password.

## Password for next level
263JGJPfgU6LtdEvgfWU1XP5yac29mFx