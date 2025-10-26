# Secret of the Polyglot

When we open the file we find the second part of the flag , then we open the same file in https://hexed.it./ then we see in the firt line that it mentions ".PNG"
<img width="835" height="159" alt="Screenshot 2025-10-26 at 4 39 59 pm" src="https://github.com/user-attachments/assets/8ee37530-ba7b-4dac-bec8-a8c77595edec" />
we save the file provided as a .png file then we get the first part of the flag 
FLAG : picoCT F[f1u3 n7-1n_pn9_&_pdf_53b741d6}

# St3g0

i used zsteg to uncover the message in the file , once running this command `zsteg -a picoctf.png` in the terminal ,  flag was indeed hidden in the LSB of the image , 
Flag : picoCTF{7h3r3_15_n0_5p00n_1b8d71db}

# 

