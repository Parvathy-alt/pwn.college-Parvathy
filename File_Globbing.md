# FILE GLOBBING


## Matching with *

When it encounters a * character in any argument, the shell will treat it as a "wildcard" and try to replace that argument with any files
that match the pattern. `/challenge/run` gives the output that `This challenge resets your working directory to /home/hacker unless you change 
directory properly...` according to which we redirect to another working directory which is `/challenge ` which is done by the line of code 
`cd /ch*` then we run `./run` to get the flag 

Flag : `pwn.college{UUvGx0arZ-6E4_ORv1veEKDK1V8.dFjM4QDLwgTN0czW}`


## Matching With ?

When the system comes across a `?` character in any argument, the shell interprets it as a wildcard that matches exactly one character,
similar to `*`, but limited to a single character.
On running `cd /?ha??enge ./run` we recive the flag .

Flag : `pwn.college{g2ZYkLXFtVpYu0hlIejBNjDZ3yJ.dJjM4QDLwgTN0czW}`


## Matching with []

As mentioned in the challenge itself "The square brackes are, essentially, a limited form of '?' " . [] is a wildcard for some subset of potential characters, specified within the brackets. For this challenge we first run ` cd /challenge/files` after which
we execute ` /challenge/run file_[absh] ` to access the file file_b, file_a, file_s, and file_h 

Flag : `pwn.college{0irKRbuJgGGWQXMI7XDMzk-A436.dNjM4QDLwgTN0czW}`


## Matching Paths with []

First we run the command `/challenge/files/file_[bash]` after which we run `/challenge/run /challenge/files/file_[bash]`
to get thr required flag .

Flag : `pwn.college{AkvpIa6ImW5IdjlCzr8F9gNpKSd.dRjM4QDLwgTN0czW}`


## Multiple Globs

We cd into  `/challenge/files` then run `/challenge/run *p*` which covers every word that contains the letter p.

Flag :`pwn.college{4VArGJDyZnHnrcDnZsa8QRQdila.QXycTO2EDLwgTN0czW}`


## Mixing Globs

The challenge asks us to first `cd` into `/challenge/files` which prints out words starting with alphabets a to z . 
We are asked to write a single, short (6 characters or less) glob that will match the files "challenging", "educational", and "pwning". 
When the command `/challenge/run [cep]*` is run we get out flag

Flag:`pwn.college{QwaDrNoOJa53L4kl3G5x4LaT8yr.dVjM4QDLwgTN0czW}`


## Exclusionary Globbing

As the name of the challenge suggests , exclusionary globbing helps us filter out files that are not relevant for our search . 
Adding " ! " or " ^ " inside the [] before the first letter of the file to filter out files that are not needed to be printed . 
First we `cd` to `/challenge/files` later we run `/challenge/run [!pwn]*` command to obtain the flag

Flag : `pwn.college{kfORaBNTGZuQQeTJJisOrlq8f0A.dZjM4QDLwgTN0czW}`


## Tab Completion

Using * for shortcuts on the command line is risky because it can expand to unintended files, especially with commands like rm. 
A safer method is tab completion, which auto-fills filenames accurately.
`cat /challenge/pwn<TAB>`

Flag :`pwn.college{sbETmo8kvKVAyfQIoLS7WiW8qDQ.QX0QTM3EDLwgTN0czW}`


## Multiple Options for Tab Completition

If a certain file has more than one number of files that start with the required variable , we first do double tab to list all the files in the directory which starts with the gives letter 
`cd /challenge`
`cat /challenge/files/pwn`
`cat /challenge/files/pwncollege-flag`

Flag:`pwn.college{EJHlBZon9qE0Dv35bNd_Sq4OGr8.QX2QTM3EDLwgTN0czW}`


## Tab Completion 

In this challenge, there’s a command beginning with pwncollege that will reveal the flag.
You must type pwncollege and use tab completion to run it
`pwncollege-18379 the-flag`

Flag : `pwn.college{kplHDhwgUn8gbf2eDDLcjXJkpPP.QX1QTM3EDLwgTN0czW}`






