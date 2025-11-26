# Lo-Fi

Tags: Web, path traversal, file inclusion<br>
https://tryhackme.com/room/lofi

## Room Description
Want to hear some lo-fi beats, to relax or study to? We've got you covered! 

Navigate to the following URL using the AttackBox: http://MACHINE_IP and find the flag in the root of the filesystem.

Check out similar content on TryHackMe:
    LFI Path Traversal
    File Inclusion

## Solution
Given a webpage displaying a discography with links to Relax, Sleep, Chill, Coffee, Vibe, Game pages. The path for each page is visible in the url, e.g. `http://10.82.185.217/?page=relax.php`

From the room description, we know we need to go to the root directory of this webserver. Going to [OWASP's path traversal](https://owasp.org/www-community/attacks/Path_Traversal) page gives path traversal attack examples. Chaining together `../` ensures we go back far enough to reach the root directory. These can replace whatever the file name is in the url.

Typing in `http://10.82.185.217/?page=../../../../../` will get us to the root directory. The flag is in here so navigate to `http://10.82.185.217/?page=../../../../../flag.txt` to print the contents of flag.txt to the webpage.

## Flag
flag{e4478e0eab69bd642b8238765dcb7d18}