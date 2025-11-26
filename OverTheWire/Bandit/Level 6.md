# Level 6

## Access for current level
Username: bandit6<br>
Password: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG (acquired from previous level)<br>
SSH command: `ssh bandit6@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
The password for the next level is stored somewhere on the server and has all of the following properties:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

## Solution
Same as before but instead of the password file being in `~`, its somewhere else on the server so we have to cd into `/`.<br>
Do the same as before but change size as per guidelines and include the user owner of the file as bandit 7. `find . -size 33c -user bandit7`<br>
Lots of files with permission denied except one so we need to cat this `cat ./var/lib/dpkg/info/bandit7.password`

## Password for next level
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj