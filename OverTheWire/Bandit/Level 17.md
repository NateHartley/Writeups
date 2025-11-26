# Level 17

## Access for current level
Username: bandit17<br>
Password: EReVavePLFHtFlFsjn3hyzMlvSuSAcRD (found in /etc/bandit_pass/bandit16 since no password was retried in previous level)<br>
SSH command: `ssh bandit17@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

## Solution
Check differences between files with the `diff` command `diff passwords.old passwords.new`. This will show which line has been changed.<br>
It shows that C6XNBdYOkgt5ARXESMKWWOUwBeaIQZ0Y has been replaced by x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO in passwords.new. We can verify this by searching for that string in passwords.new `grep "x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO" passwords.new".

## Password for next level
x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO