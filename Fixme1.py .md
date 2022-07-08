<h1>Fixme1.py</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/240">click here</a>
<h2>Overview</h2>
<b>Points</b> - 100<br>
<b>Skills tested</b> - General skills(Python Programming)
<h2>Problem</h2>
Fix the syntax error in this <a href="https://artifacts.picoctf.net/c/38/fixme1.py">Python script</a> to print the flag.
<h2>Approach</h2>
Download the Python script from <a href="https://artifacts.picoctf.net/c/38/fixme1.py">here</a><br>
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


flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + chr(0x07) + chr(0x00) + chr(0x46) + chr(0x0b) + chr(0x1a) + chr(0x5a) + chr(0x1d) + chr(0x1d) + chr(0x2a) + chr(0x06) + chr(0x1c) + chr(0x5a) + chr(0x5c) + chr(0x55) + chr(0x40) + chr(0x3a) + chr(0x5e) + chr(0x52) + chr(0x0c) + chr(0x01) + chr(0x42) + chr(0x57) + chr(0x59) + chr(0x0a) + chr(0x14)

  
flag = str_xor(flag_enc, 'enkidu')
  print("That is correct! Here's your flag: " + flag)
</pre>
You can either run this on an IDE or on the webshell <a href="https://webshell.picoctf.org/">provided by PicoCTF</a><br>
As you may observe, the error is in the last line where the <i>print</i> statement hasn't been indented properly
After indernting it and running the program, you will see this on the screen
<pre>That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}</pre>
<pre>picoCTF{1nd3nt1ty_cr1515_09ee727a}</pre>
Type in the flag and you're done.
