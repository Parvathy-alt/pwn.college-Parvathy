 # TERMINAL MULTIPLEXING 

 ## Launching Screen 

 The challenge required starting a screen session; the challenge infrastructure is set up so that launching screen immediately presents the flag.
 `screen`
 Flag:`pwn.college{MQDrf69Oui-A-HA9KgCmM3xJFSL.QX1gjM4EDLwgTN0czW}`

 ## Detaching and Attaching 

 We learn how to detach the screen using Ctrl A and then d and reattach it using screen -r
 Flag : ` pwn.college{kWpbFn2OrjolP2r0U4yiOiWKPdJ.QX2gjM4EDLwgTN0czW}`

 
 ## Finding Sessions 

 First we list all the sessions in the screen by writing `screen -ls` and then we choose one detached session and reattach it `150.session_cc857ee8ef870f9e`
 Flag : `pwn.college{84mHpv1OqtE0Kg43UtOYuilZ027.QX3gjM4EDLwgTN0czW}`


 ##  Switching Windows 

 We access alll the sessions in screen and then attach the detached session then we switch from window 1 to window 0 using the command `Ctrl A 0`
 Flag : `pwn.college{A90IIlnyKvlhHRIxr072XXBLAuq.QX4gjM4EDLwgTN0czW}`


 ## Detaching and Attaching (tmux)

We first start the tmux session and then detach from the session by typing Ctrl B and then d and then then `/challenge/run` then we'll get a message saying the flag is attached to the session ;
so we reattach the session by typing `tmux attach`. 
Flag:`pwn.college{s_CXW9t3KxQAy0_oq9P4qhb41E3.QX5gjM4EDLwgTN0czW}`

## Switching Windows (tmux)

First you list all the tmux sessions by the command `tmux ls` then you attach the session and then switch to window 0 then detach and we'll get the flag.
Flag :`pwn.college{wFiQPa4xZxuOEmOdXgkGhUPsUl3.QXwkjM4EDLwgTN0czW}`

 
