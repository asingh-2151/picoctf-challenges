<h1>HashingJobApp</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/243">click here</a>
<h2>Overview</h2>
<b>Points</b> - 100<br>
<b>Skills tested</b> - General skills(Shell/command line + Netcat + MD5 hashing + Python programming)
<h2>Problem</h2>
If you want to hash with the best, beat this test!
<pre>nc saturn.picoctf.net 63116</pre>
<h2>Approach</h2>
Here, you will first need to have a program to convert text into MD5 hashes. I would recommend to use Python.<br>
This was my program in Python
<pre>import hashlib
s=str(input())
res=hashlib.md5(s.encode())
print(res.hexdigest())</pre>
With this Python code in a notebook (colab or Jupyter), enter the <a href="https://webshell.picoctf.org/">PicoCTF Webshell</a>.
Once in there, enter the below line in the terminal.
<pre>nc saturn.picoctf.net 63116</pre>
<b>Disclaimer</b>-Now you will have to pass three challenges of converting text inside quotes provided by the server as an MD5 hash. The three phrases/names/words will differ for everyone, the below attempt is what I received in my test. Also ensure that you answer the question corretly within <b>two</b> attempts as it logs out of the netcat if you can't. Finally, ensure that you answer each question within <b>45 seconds</b>.
<br>You will now see on the screen
<pre>Please md5 hash the text between quotes, excluding the quotes: 'Cindy Crawford'
Answer: 
</pre>
The answer for this is
<pre>2ee8ebf845baa7f500e153417cf691fd</pre>
Enter it in the terminal and you will get the next question
<pre>
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'coconuts'
Answer:
</pre>
The answer for this is
<pre>
78d1999482f432e9c229269151140542
</pre>
Enter it in the terminal and you will receive the final question
<pre>
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'corn on the cob'
Answer:
</pre>
The answer for this is
<pre>
4d26abd4924cfb39c48f7841dd579c0d
</pre>
You will finally see on the screen
<pre>Correct.
picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}</pre>
This gives us the flag as
<pre>picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}</pre>
Type in the flag and you're done.
