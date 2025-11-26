# Level 9

## Access for current level
Username: bandit9<br>
Password: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM (acquired from previous level)<br>
SSH command: `ssh bandit9@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

## Solution
Given a file full of jargon letters, the password is the only human-readable text in there, and it follows a bunch of === to make it stand out.<br>
We can use `strings` to return all the human-readable text from a file. `strings data.txt`

## Password for next level
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey