# PROCESSES AND JOBS 


## Listing Processes

We learned about ps command which stands for "process snapshot" or "process status" , it allows us to monitor the status of running processes on a system . We can use arguments to follow
along the ps command such as " ps -ef" and "ps aux"
To successfully complete the following challenge we run the command : 
`ps -ef`
From which we run the command `/challenge/27974-run-6586` 

Flag: `pwn.college{8VzuePiJM-fTF4nfkLMzTItBVKP.dhzM4QDLwgTN0czW}`


## Killing Processes

We learn abou `kill` and `sleep` command 
`/challenge/dont_run` must be killed before `/challenge/run` is executed so that the flag can be obtained 
The PID of `/challenge/dont_run` is found by using the ps
The command is as follows : `ps -ef | grep /challenge/dont_run`
The next command is as follows : 
` kill 73`
`/challenge/run`

Flag : `pwn.college{8Wk2pw-j9xI0e66Tdtq0S4qVxj8.dJDN4QDLwgTN0czW}`

## Interrupting Processes

When we run `/challenge/run` command ,this is the output obtained :
`I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!`
Hence we use `Ctrl` command and press `c` .

Flag : `pwn.college{0jUTH_pOxrUodvIgHj1PdeaJXoA.dNDN4QDLwgTN0czW}`

## Suspending Processes

We learned in the previous challenge to interrupt the process we can use `Ctrl-c` , processes can be suspended by using `Ctrl-z`
In this challenge , we will first run the command `/challenge/run' `
Then we use the hotkey `Ctrl-c` and later `Ctrl-z`, then we run `/challenge/run` again to get the flag

Flag : `pwn.college{s9MN8cyYTgJisTFHIvzuQRsTpi3.dVDN4QDLwgTN0czW}`

## Resuming Processes

As the name of the challenge suggests we us `fg` comamnd to resume the processes that we have suspended 
We first run `/challenge/run` and then suspend it by using the hotkey `Ctrl-Z` and then enter `fg` to resume it to get the flag .

Flag : `pwn.college{gkvZHIUByVyVFdkXSoH9fcwdpPx.dZDN4QDLwgTN0czW}`

## Backgrounding Processes

The flag is only provided if there exists another copy of `/challenge/run` running and not suspended in the terminal. 
We run `bg` command for the same and run `/challenge/run` again after which we get teh flag .

Flag : `pwn.college{IqbfTx4YRKPbEDT8ofpUwZClRdY.ddDN4QDLwgTN0czW}`

## Foregrounding Processes

To pass this challenge we first suspend the process using the `Ctrl-Z` hotkey after which we use `bg` to run it in the baground ,
then to resume into the foreground process we enter `fg` which will give us the flag .

Flag : `pwn.college{4OzLarps0et2uvuksSvHmAHipK5.dhDN4QDLwgTN0czW}`

## Startinf Bagrounding Processes

As the name of the challenge suggests we can directly baground the process by adding `&` to the end of the command propmt 
The command required to get the flag is as follows : `/challenge/run &`

Flag : `pwn.college{UffNiPk-3DkaeexkVw8lsQOP0WZ.dlDN4QDLwgTN0czW}`

## Process Exit Codes

First we run `/challenge/get-code` after which run `/challenge/submit-code` with error code (`$?`) as an argument ie `/challenge/submit-code $?`

Flag : `pwn.college{cYx9A7sf8VOy-FwlAU6kLlvHVFK.dljN4UDLwgTN0czW}`
