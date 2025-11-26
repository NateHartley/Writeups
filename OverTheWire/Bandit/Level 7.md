# Level 7

## Access for current level
Username: bandit7<br>
Password: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj (acquired from previous level)<br>
SSH command: `ssh bandit7@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
The password for the next level is stored in the file data.txt next to the word millionth

## Solution
Given one file with a long list of words, our password is next to the word “millionth”.<br>
`grep “millionth” data.txt` will print the instance of millionth and everything else on that line which includes the password.

## Password for next level
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc