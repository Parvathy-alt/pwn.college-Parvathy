# Uuntangling Users

## Becoming Root With Su

As the name of the challenge suggests we can become the root user using `su` command , after which the password will be asked which is 
: `hack-the-planet` , then we use `cat /flag` to get the flag .

Flag : `pwn.college{gdgPpDvuzPlIH-0GHkaJ2S-r0Ab.dVTN0UDLwgTN0czW}`

## Other Users With su

In this challenge we will switch to user called "zardus" for which we will run the command : `su zardus` , and enter the password : `dont-hack-me` then run `/challenge/run` to get the flag

Flag : `pwn.college{kZTGrDDtGL3643WgW97Amh1yuJ3.dZTN0UDLwgTN0czW}`

## Cracking Passwords

To access `/challenge/shadow-leak` we run the command , `john /challenge/shadow-leak` which gives us the password for user "zardus" which is ,
`aardvark ` after which we run `/challenge/run` to get the flag . 

Flag : `pwn.college{YKX4IqW8kcFHgxEPhfuXtOeLxRi.ddTN0UDLwgTN0czW}`

## Using Sudo

We have sudo permsission in this challenge hence we run `sudo cat /flag` to obtain the flag .

Flag : `pwn.college{A5Ohfa5FWpIEqpGm-LjSRoD9XG9.dhTN0UDLwgTN0czW}`
