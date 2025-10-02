# PONDERING PATH 


## The PATH Variable 

On running ` /challenge/run` the flag gets deleted hence we empty the PATH variable ,`PATH=""` now running  ` /challenge/run` we get the flag 

Flag : `pwn.college{oN7rAwXAkq9B1R70Ik_Z8WBeoG_.dZzNwUDLwgTN0czW}`


## Setting PATH 

`win` is in `/challenge/more_commands/` we need to add it to PATH which can be done by `PATH="/challenge/more_commands/"` , then running `/challenge/run` gives the flag 

Flag : `pwn.college{IhPKpEgCSVLHHRPGzZrrkw6oC54.dVzNyUDLwgTN0czW}`


## Finding Commands 
` which win` command gives you the directory which is  `/challenge/paths/21754/win` then you `cat /challenge/paths/21754/flag`

Flag : `pwn.college{MysHeFoR8U2atyZknZZsYm3F5cc.QX3MTM3EDLwgTN0czW}`


## Adding Commands

First we make the directory called `windir` : `mkdir windir` then we change directory using ` cd windir` . After which we create `win` using `nano` and enter `cat /flag` to the file .
Then we use `chmod +x win` to make the file accessible and `echo $PATH` to find the loaction of the flag , then to change to PATH variable `PATH="/usr/bin:/home/hacker/windir"` 
Finally we run ` /challenge/run` to get the flag .

Flag : `pwn.college{QolCviHcvq4cvYahzJaivK63Shi.dZzNyUDLwgTN0czW}`


## Hijacking Commands

We first make a directory called `hack` using `mkdir` after which we run the command `nano hack/rm` and then to make it successful `chmod +x hack/rm` later  `export PATH="hack/rm:$PATH"` and finally  `/challenge/run` to get the flag 
Flag : `pwn.college{E32hco8xgPQjMsO3BxwdDGoyy2v.ddzNyUDLwgTN0czW}`
