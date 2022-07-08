<h1>Convertme.py</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/239">click here</a>
<h2>Overview</h2>
<b>Points</b> - 100<br>
<b>Skills tested</b> - General skills(Decimal to binary conversion,Python Programming)
<h2>Problem</h2>
Run <a href="https://artifacts.picoctf.net/c/30/convertme.py">the Python script</a> and convert the given number from decimal to binary to get the flag.
<h2>Approach</h2>
Download the Python script from <a href="https://artifacts.picoctf.net/c/30/convertme.py">here</a><br>
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
flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5f) + chr(0x05) + chr(0x08) + chr(0x2a) + chr(0x1c) + chr(0x5e) + chr(0x1e) + chr(0x1b) + chr(0x3b) + chr(0x17) + chr(0x51) + chr(0x5b) + chr(0x58) + chr(0x5c) + chr(0x3b) + chr(0x42) + chr(0x53) + chr(0x5c) + chr(0x0d) + chr(0x5e) + chr(0x50) + chr(0x4d) + chr(0x00) + chr(0x13)
num = random.choice(range(10,101))
print('If ' + str(num) + ' is in decimal base, what is it in binary base?')
ans = input('Answer: ')
try:
  ans_num = int(ans, base=2)
  if ans_num == num:
    flag = str_xor(flag_enc, 'enkidu')
    print('That is correct! Here\'s your flag: ' + flag)
  else:
    print(str(ans_num) + ' and ' + str(num) + ' are not equal.')
except ValueError:
  print('That isn\'t a binary number. Binary numbers contain only 1\'s and 0\'s')
</pre>
You can either run this on an IDE or on the webshell <a href="https://webshell.picoctf.org/">provided by PicoCTF</a><br>
On running the program, you will see this on the screen
<pre>If X is in decimal base, what is it in binary base ?
Answer:</pre>
where X can be any random (mostly 2-digit) number.<br>
You can either use a <a href="https://www.rapidtables.com/convert/number/decimal-to-binary.html">decimal-to-binary conversion calculator</a> or solve this by hand.<br>
On entering the correct answer, you will see this on the screen
<pre>That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_762f748e}</pre>
This gives us the flag as
<pre>picoCTF{4ll_y0ur_b4535_762f748e}</pre>
Type in the flag and you're done.
