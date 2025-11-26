# Level 8

## Access for current level
Username: bandit8<br>
Password: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc (acquired from previous level)<br>
SSH command: `ssh bandit8@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once.

## Solution
Given a huge list of random strings, the password is the only string that appears only once in the file.<br>
We can use `uniq` to get the unique line but must use the `-u` flag. But before that we need to sort the list then pipe that into the `uniq` command. <br>
`sort data.txt | uniq -u`

## Password for next level
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM