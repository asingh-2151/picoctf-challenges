<h1>Fixme2.py</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/241">click here</a>
<h2>Overview</h2>
<b>Points</b> - 100<br>
<b>Skills tested</b> - General skills(Python Programming)
<h2>Problem</h2>
Fix the syntax error in this <a href="https://artifacts.picoctf.net/c/67/fixme2.py">Python script</a> to print the flag.
<h2>Approach</h2>
Download the Python script from <a href="https://artifacts.picoctf.net/c/67/fixme2.py">here</a><br>
On opening the file, you will see this code
<pre>import random



def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])


flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x58) + chr(0x18) + chr(0x11) + chr(0x41) + chr(0x09) + chr(0x5f) + chr(0x1f) + chr(0x10) + chr(0x3b) + chr(0x1b) + chr(0x55) + chr(0x1a) + chr(0x34) + chr(0x5d) + chr(0x51) + chr(0x40) + chr(0x54) + chr(0x09) + chr(0x05) + chr(0x04) + chr(0x57) + chr(0x1b) + chr(0x11) + chr(0x31) + chr(0x0d) + chr(0x5f) + chr(0x05) + chr(0x40) + chr(0x04) + chr(0x0b) + chr(0x0d) + chr(0x0a) + chr(0x19)

  
flag = str_xor(flag_enc, 'enkidu')

# Check that flag is not empty
if flag = "":
  print('String XOR encountered a problem, quitting.')
else:
  print("That is correct! Here's your flag: " + flag)
</pre>
You can either run this on an IDE or on the webshell <a href="https://webshell.picoctf.org/">provided by PicoCTF</a><br>
As you may observe, the error is in the fourth line from below where the <i>==</i> expression has been instead written as <i>=</i>.<br>
After correcting it and running the program, you will see this on the screen
<pre>That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}</pre>
This gives us the flag as
<pre>picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}</pre>
Type in the flag and you're done.
