# Level 13

## Access for current level
Username: bandit13<br>
Password: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn (acquired from previous level)<br>
SSH command: `ssh bandit13@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

## Solution
Use private ssh key provided to log into next account.<br>
`ssh -i ./sshkey.private bandit14@bandit.labs.overthewire.org -p 2220`

## Password for next level
(no password but a private key instead)<br>