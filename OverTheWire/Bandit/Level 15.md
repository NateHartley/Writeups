# Level 15

## Access for current level
Username: bandit15<br>
Password: 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo (acquired from previous level)<br>
SSH command: `ssh bandit15@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.

## Solution
We can use `openssl` with the `s_client` command as this is a generic SSL/TLS client which connects to a remote host using SSL/TLS.<br>
We can echo our previous password into `openssl s_client` for it to be ecnrypted and then sent to localhost. We can also include the `-ign_eof` to keep the connection open so we can read the response.<br>
`echo "8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo" | openssl s_client -connect localhost:30001 -ign_eof`

## Password for next level
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
