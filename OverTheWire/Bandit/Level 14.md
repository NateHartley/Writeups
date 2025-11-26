# Level 14

## Access for current level
Username: bandit14<br>
Password: MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS (found in /etc/bandit_pass/bandit14 since no password was retried in previous level)<br>
SSH command: `ssh bandit14@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

## Solution
Instructed to upload the current password to localhost on port 30000 to get the next password.<br>
Use telnet to set up a connection. `telnet localhost 30000` Then paste in current password.

## Password for next level
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo