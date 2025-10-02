# PONDERING PATHS


## The Root

In this challenge we learned how to invoke a program by providing its path on the command line. We also learned that when  the root starts with root directory is called absolute path ,
and the challenge was to invoke the pwn program using its absolute path which can be done by entering `/pwn`. 

Flag : `pwn.college{cHF_BYmWNvlZuPto_FKXAoiW14x.dhzN5QDLwgTN0czW}`

## Programs and Absolute Paths 

The challenge is located in the root-mounted `challenge` directory. The task for this level was to run the challenge program named `run`, which resides at `/challenge/run`.
Executing the program using its absolute path prints a flag that indicates successful completion.

Flag :`pwn.college{gzDICrbC_ZnjaubK9P3NGM3D9j3.dVDN1QDLwgTN0czW}`


## Positin Thyself 

The challenge asks us to go to you `\home` direectory to run the command `\challenge\run`
Hence the commands are as follows : 
`cd /home`
`\challenge\run`

Flag : `pwn.college{M1-ARB3nm3gy0aDeo4t146GedD2.dZDN1QDLwgTN0czW}`


## Position Elsewhere

Similar to the previous challenge , once we run the command `/challenge/run` they ask us to go to `/usr/bin` 
To do that : `cd /usr/bin ` 
After which we run the command : `/challenge/run` to get the flag 

Flag : `pwn.college{Iz7NJ0ry8UB1uN5aldFh-OOHJaH.ddDN1QDLwgTN0czW}`


## Position Yet Elsewhere

Similar to the previous challenge we'll be ask to access `/usr/include` directory to successfully run the `/challenge/run` command and get the flag :
`cd  /usr/include`
 `/challenge/run`
 
 Flag : `pwn.college{gKqhsKsqEM6dqcoB4pZRGwyOH9E.dhDN1QDLwgTN0czW}`


## Implicit Relative Paths , From /

In this challenge we learn about relative paths , The challenge description specifies that `/challenge/run` must be invoked from a relative path to do so : 
`cd /`
`challenge/run`

Flag : `pwn.college{sikimQsmv48ge8NKb2WOxUEHtzY.dlDN1QDLwgTN0czW}`

## Explicit Relative Paths , From /

Similarly we learn about explicit path , which needs to be accessed to get the flag 
`cd /`
`./challenge/run`

Flag : `pwn.college{Q6in2zJZ7IUNBWdf9HNkMVDo-aE.dBTN1QDLwgTN0czW}`

## Implicit Relative Path

We have to run the challenge from the `/challenge` directory and we should explicitly run the `run` command to get the flag 
`cd /challenge`
`./run`

Flag : `pwn.college{kOwDEASySkSTGL_AmKspbkiSxBL.dFTN1QDLwgTN0czW}`

## Home Sweet Home 

In this challenge we are asked to run the command `/challenge/run` in some absolute path of some direcotry , we can use `~` as a expansion of 
home directory 
We run the following command to attain the flag ,
`/challenge/run ~/h` where is the `h` is the file that I specifiy as an arugment 

Flag : `pwn.college{E8oTro5nLkAx_pGgLNwJpwEBJWK.dNzM4QDLwgTN0czW}`



