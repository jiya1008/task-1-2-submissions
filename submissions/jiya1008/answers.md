name= Jiya Jain

roll\_no= 16014024022

branch= EXCP

mail= jiya31@somaiya.edu

phone= 9826441116



#### Task 1 - Linux Installation \& Linux Journey

screenshots attached



##### What I Learned:

Linux filesystem basics

Navigation commands

Permissions

Processes

Package management



#### Task 2 - OverTheWire Bandit

screenshots attached for each level



##### explanation of each level:

###### Level 0: ssh bandit0@bandit.labs.overthewire.org -p 2220

* The task was clearly given in the game instruction so this was a direct command 



###### Level 0-1: Password found: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

* The password was in the readme file in home directory, the commands for this was also learnt by doing the labs and reading theory for the task 1 grasshopper of linux. Simply using ***ls*** worked and there was only one file so simply using ***cat*** showed the contents of the file.



###### Level 1-2: Password found: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

* Here the file was a dash so it took a few tries to figure out the command, had to use ***cat*** for sure because the file is a plain and readable but the dash is also a command like in ***-p*** so I knew I couldn’t simply write it and hence finally I used ***./-*** . 



###### Level 2-3: Password found: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

* I honestly had to google this one because I couldn’t figure out after the ***cat*** command.



###### Level 3-4: password found: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

* Since this level included a directory, first I used ***cd*** to get into that directory then since the file is hidden so I used its command which I learnt from grasshopper labs. Here the colors helped me identify clearly the name of the file as the starting 3 dots are blue in color so I knew they represent “inside a directory”.



###### Level 4-5: password found: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

* As instructed in the game, they gave a  hint, “Tip: if your terminal is messed up, try the “reset” command.” So when I used the ***ls*** command to check the files, seeing so many files I knew that if I randomly open a file it might crash or mess up my terminal, so first I checked the filetypes and then opened only the correct file. I was doubtful between file05 and file07, so I read about them and hence opened file07 only.



###### Level 5-6: password found: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG



###### Level 6-7: password found: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

* ***/***: Tells the system to start the search from the very top (the root) of the entire server.
* ***-user bandit7***: Searches specifically for a file owned by user bandit7.
* ***-group bandit6***: Searches specifically for a file owned by group bandit6.
* ***-size 33c***: Searches for a file that is exactly 33 bytes in size.
* (this I had to google) ***2>/dev/null***: This is a pro-tip for rookies! Because you are searching the whole server, the system will try to look in folders you don't have permission to access, which will result in many "Permission denied" errors. This part of the command hides all those annoying error messages so you can focus only on the result you need.



###### Level 7-8: password found: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

* So since data.txt file could have the password anywhere and they gave a hint that password is next to the millionth word and in the commands that can be used I found ***grep***, I know ***grep*** would give me the whole line where the word millionth is written, so when I ran it, surprisingly the line contained password and that word only.



###### Level 8-9: password found: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

* So this time I had to find a line that is unique, in commands it suggested ***sort*** and ***uniq***, using those I thought I will first ***sort*** then run the ***uniq*** command to find that unique line but it doesn’t work that way and all I got was just the sorted lines, the ***uniq*** command did not show any result, then I read about it in the helpful reading material of the challenge and realized that’s not how the ***uniq*** command works and so I ran them both together as combined command, that is piping.



###### Level 9-10: password found: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

* Again I ran the ***grep*** with just “==” and it only showed that yes the file matches but no clear password, then I re-read the hint on the challenge and realized I need to use ***strings*** as not whole data is in human readable, just a very few part of it is and I need to find that specific part and hence I used piping again.



###### Level 10-11: password found: dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

* I know to decode I can use ***-d*** command but I didn’t quite know how to solve this one, so I had to use AI to understand this one.



###### Level 11-12: password found: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

* So this one has been ciphered by ROT13, and I need to reverse it. I had to read about how to reverse the characters, the commands given in the hint, from ***tr*** made some sense to me for this challenge. I could use this command to change the characters, so I had to shift all by 13 characters, meaning changing A to N, B to O and so on.. Then I looked into how to use the command, its syntax and done.



###### Level 12-13: password found: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

* I got quite stuck on this one, confused which command to run first, after reading and using AI, still it was tricky and then I ultimately followed how AI told and understood the explanation from it. So when I ran ***ls*** and found data.txt file and ran ***file*** to see what type of content it had, it showed ASCII so I thought that’s the correct file but it was not so I got more confused and when I decompressed the data6.bin file it just kept going to data7.bin then data8.bin then data9.bin so I thought it was a catch, but then AI told me that it was the correct path so I tried once more and decompressed data9.bin and ran ***ls*** and turns out the data9.bin was not there and no more data10.bin either. Hence I knew the task was done! And I just had to check the listed files to find the ASCII content file.



###### Level 13-14: password found: RSA key, no password

* Since there was no password on this level, opening the files HINT and sshkey.private gave me everything I was looking for, I found the RSA key, so I knew that this is cryptographic method for sharing of data, using this key I had to login on next level as bandit14. First I tried login from the sthere only and it gave the error something related to a server, so I thought that I am not on the right server, so from those error I found the correct server and tried login then but that did not work either then I realized I need to login via different place as this place is already recognized as the first start point, so I logged in through my own laptop after saving the file for RSA key, and used it during my login as my identity through the command ***-i bandit14.key*** and it worked!



###### Level 14-15: password found: MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

* here using the ***cat*** command to read this level files gave me the password directly for this level, as I had already required the access for level 14 in the previous level, so I can view the files of level 14 and find the password in it.



###### Level 15-16: password found: 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

* now I just had to use the level 14 password and send it to localport using ***echo*** command, this password worked as my key and local port replied level 15 replied back with its password as the answer to my correct key.