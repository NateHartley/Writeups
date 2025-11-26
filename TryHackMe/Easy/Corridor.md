# Corridor

Tags: Linux, web, IDOR, hash
https://tryhackme.com/room/corridor

## Room Description
You have found yourself in a strange corridor. Can you find your way back to where you came?

In this challenge, you will explore potential IDOR vulnerabilities. Examine the URL endpoints you access as you navigate the website and note the hexadecimal values you find (they look an awful lot like a hash, don't they?). This could help you uncover website locations you were not expected to access.

## Solution
Website shows a corridor of doors, each door redirects you to another page displaying a picture of an empty room.

Each link has a string of random characters and of the same length at the end. Clues in the description of the challenge inform us that these strings are hashes. Identify hashes as MD5. Convert these strings from MD5 to ascii and they are all numbers from 1 to 13 excluding 8.

This challenge wants us to exploit an IDOR vuln, so we need to edit the url in some way to redirect us to a page we shouldn't be able to access. We can start by going to the number 8 page that was missing from our list. Convert 8 to MD5 hash and add this to link. Try it and it leaves us to another empty room. Try 14 instead, no luck. Try 0, redirects us to a page displaying the flag.

## Flag
flag{2477ef02448ad9156661ac40a6b8862e}