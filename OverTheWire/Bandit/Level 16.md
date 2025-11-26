# Level 16

## Access for current level
Username: bandit16<br>
Password: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx (acquired from previous level)<br>
SSH command: `ssh bandit16@bandit.labs.overthewire.org -p 2220`<br>

## Level Goal
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.

## Solution
First we need to check how many ports are open between 31000-32000 on this vm so we can use nmap. `nmap localhost -p 31000-32000`<br>
From here we get back 5 open ports (31046, 31518, 31691, 31790, 31960). Now we need to check which ones are using SSL/TLS.

We can use the ssl-enum-ciphers script which gives us back SSL/TLS info from a service, but if it doesn't support it then it won't return anything.<br>
Running this command `nmap localhost --script ssl-enum-ciphers -p 31046,31518,31691,31790,31960` we can see that the only services that give us back any info are for ports 31518 and 31790.

Now we can use the same command as last time on both ports to see which is the correct one. Port 31518 will only give us back what we echoed in so this isn't the right one, but port 31790 is correct.

Running this `echo "kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx" | openssl s_client -connect localhost:31790 -ign_eof` will give us a private RSA key that we need to decrypt.

So we now need to use this RSA private key to ssh into the next level. We need to save the key to a file, but we don't have write permission in the home directory so we can just make a file in the /tmp directory.

Now finally we can use this private key to ssh into the next challenge `ssh -i /tmp/my_key bandit17@bandit.labs.overthewire.org -p 2220`

But we get an error that our key is too open and it won't connect use. So we need to limit permissions on this key file and try connect again `chmod 600 /tmp/my_key`

## Password for next level
EReVavePLFHtFlFsjn3hyzMlvSuSAcRD
