# CHAINING COMMANDS

## Chaining with Semicolon 

We chain `/challenge/pwn` and `/challenge/college` using `;` the required command to get the flag is : `challenge/pwn; /challenge/college`
Flag : `pwn.college{8RZC24OT5hjRdN_fG--z6JAJqdI.dVTN4QDLwgTN0czW}`

## Building on Success

AND operator &&  is used such that the second program runs only if the first one succeeds.
` /challenge/first-success`
`/challenge/first-success && /challenge/second`
Flag : `pwn.college{cM8qIQsDocOUiQfV6sDjP9QVrG0.QXyQzM4EDLwgTN0czW}`

## Handling Failure

OR operator ||: run the second command only if the first command fails.
`/challenge/first-failure || /challenge/second`
Flag: ` pwn.college{U1vPU9IhdpEAw8xSBH1TsUNsIur.QXzQzM4EDLwgTN0czW}`

## Your First Shell Script

First we create `x.sh` using `nano` command like so , `nano x.sh` then run the command : `/challenge/pwn` and `/challenge/college` and then run `bash x.sh` to get the flag 
Flag : `pwn.college{waVKfWADgPRGfCnqdHH4w73bimN.dFzN4QDLwgTN0czW}`

## Redirecting Script Output

Th output of `x.sh` is piped into ` /challenge/solve` which can be done by the command , `bash x.sh | /challenge/solve` 
Flag : `pwn.college{IhoPPJy1TA9uL1gGl5KB12Q3iOi.dhTM5QDLwgTN0czW}`

## Eexecutable Shell Scripts

We create a script called `script.sh` using `nano`in which we enter the command `/challenge/solve` after saving we enter `chmod +x script.sh` and run it using ` ./script.sh` 
Flag : `pwn.college{4oAMh8eBbdzIBbhn6MTN-NL08pZ.dRzNyUDLwgTN0czW}`

## Understanding Shebangs

Flag:`pwn.college{ocVgap2XJIXg0QIT_adK0TR0l5c.QX5MzM4EDLwgTN0czW}`

## Scripting With Arguments 

Flag : `pwn.college{sDJvmiV_Ma488SZCnt2vYRUVTa5.QX1MzM4EDLwgTN0czW}`
