<h1>Based</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/35">click here</a>
<h2>Overview</h2>
<b>Points</b> - 200<br>
<b>Skills tested</b> - General skills(Netcat + Conversion between Number Systems + ASCII)
<h2>Problem</h2>
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with <pre>nc jupiter.challenges.picoctf.org 29221</pre>
<h2>Approach</h2>
Since this exercise entails conversion between number systems and then to ASCII characters, we will need calculators to do so.<br>
Here are the three main calculators which can help in this task:-<br>
<a href="https://www.rapidtables.com/convert/number/binary-to-ascii.html">Binary to text converter</a><br>
<a href="https://onlineasciitools.com/convert-octal-to-ascii">Octal to text converter</a><br>
<a href="https://www.rapidtables.com/convert/number/hex-to-ascii.html">Hexadecimal to text converter</a><br>
Enter the command in the <a href="https://webshell.picoctf.org/">PicoCTF Webshell</a>
<pre>nc jupiter.challenges.picoctf.org 29221</pre>
<b>Disclaimer</b>-Now you will have to pass three challenges of converting numbers provided into text via the ASCII system. The three words will differ for everyone, the below attempt is what I received in my test. Also ensure that you answer the question corretly within <b>two</b> attempts as it logs out of the netcat if you can't. Finally, ensure that you answer each question within <b>45 seconds</b>.<br>
You will now see on the screen a binary to text conversion problem
<pre>
Let us see how data is stored
Please give the 01101110 01110101 01110010 01110011 01100101 as a word.
...
you have 45 seconds.....
Input:
</pre>
You will get the answer as
<pre>nurse</pre>
Type in the answer, and you will see on the screen an octal to text conversion problem.
<pre>
Please give me the  143 157 156 164 141 151 156 145 162 as a word.
Input:
</pre>
You will get the answer as
<pre>
container
</pre>
Type in the answer, and you will receive the final question on the screen - a hexadecimal to text conversion problem.
<pre>
Please give me the 737472656574 as a word.
Input:
</pre>
You will get the answer as
<pre>
street
</pre>
Type in the answer, and you will see on the screen finally this
<pre>
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}</pre>
From this, we get the flag as
<pre>picoCTF{learning_about_converting_values_00a975ff}</pre>
Type in the flag and you're done.
