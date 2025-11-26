# Level 12

## Access for current level
Username: bandit12<br>
Password: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4 (acquired from previous level)<br>
SSH command: `ssh bandit12@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Solution
Given a hexdump thats been compressed several times.<br>
We can use `mktemp -d` to automatically make a temporary folder in the `/tmp/` directory. We have to decompress from a bunch of different compression methods: tar, gzip, bzip2.<br>

For tar<br>
`mv input input.tar`<br>
`tar xf input.tar`<br>

For gzip<br>
`mv input input.gz`<br>
`gzip -d input.gz`<br>

For bzip2<br>
`mv input input.bz2`<br>
`bzip2 -d input.bz2`<br>


## Password for next level
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn