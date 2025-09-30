# SHELL VARAIBLES 

## Printing  Variables

In this challenge we run the command `echo $FLAG` to get the flag , we use`$` to prepend the variable name 
Flag : `pwn.college{0senXPLbuWZnwzPq84jUG6BWMr6.ddTN1QDLwgTN0czW}`

## Setting Variables

We learn how to assign values to variables using `=` operator 
The command to get the flag is as follows : `PWN=COLLEGE`
Flag : `pwn.college{0vwbsDyPbgzf9hrc0WURGfn5A0C.dlTN1QDLwgTN0czW}`

## Multi Word Variables 

We assign multiple values to a variable in this challenge 
Command is as follows : `PWN="COLLEGE YEAH"`
Flag:`pwn.college{Qwkm_Dyo6EgN4QXpNHISntN2Wz-.dBjN1QDLwgTN0czW}`

## Exporting Variables

In this challenge we are asked to export variable `PWN` to value `COLLEGE` and set `COLLEGE` to `PWN`
The commands for the following are : 
` export PWN=COLLEGE`
`COLLEGE=PWN`
`Flag : pwn.college{kNzCBIT5-RUtn3Kzi-dvBabjACJ.dJjN1QDLwgTN0czW}`

## Printing Exported Variables

We learn about `env` command which helps us print out every exported variable set in your shell , amongst which we find the flag 
Flag : `pwn.college{gtzNb2xt9rQIXCd1yCEUH-GMYSY.dhTN1QDLwgTN0czW}`

## Storing Command Output

As the name of the challenge suggests we store the output of `/challenge/run` in `PWN` variable
The commands go as follows : 
` PWN=$(/challenge/run)`
Output : ```Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!```
`echo $PWN`
Flag : `pwn.college{0E8EJ_DuLpeAHfSLp2YJZiuO0fz.dVzN0UDLwgTN0czW}`

## Reading Input

The format for reading inputs and assign it to a varibale is as follows:
`hacker@dojo:~$ read -p "INPUT: " MY_VARIABLE`
In this challenge we are asked to input "COLLEGE" as the input and assign it to the variable "PWN"
```    read -p "INPUT:" PWN```
```    INPUT:COLLEGE```
  ```  You've set the PWN variable properly! As promised, here is the flag:```
Flag :```pwn.college{QJixVf6GNQb3m9x0AB9IsFgJL9u.dhzN1QDLwgTN0czW}```


## READING FILES 

We are asked to  read `/challenge/read_me` into the `PWN` environment variable
That can be done by running the  following code :
```read PWN < /challenge/read_me```
The output is : 
```You've set the PWN variable properly! As promised, here is the flag:```
Flag :```pwn.college{47BTz1bvYDs03O8J0HP5ubGR36k.dBjM4QDLwgTN0czW}``
