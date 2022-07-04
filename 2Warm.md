<h1>2Warm</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/86">click here</a>
<h2>Overview</h2>
<b>Points</b> - 50<br>
<b>Skills tested</b> - General skills(Decimal to binary conversion)
<h2>Problem</h2>
Can you convert the number 42 (base 10) to binary (base 2) ?
<h2>Approach</h2>
You can either use a <a href="https://www.rapidtables.com/convert/number/decimal-to-binary.html">decimal-to-binary conversion calculator</a> or solve this by hand.<br>
<pre>42=(2*21)+0<br>
21=(2*10)+1<br>
10=(2*5)+0<br>
5=(2*2)+1<br>
2=(2*1)+0<br>
1=(1*0)+1
</pre>
Going from bottom to the top, we get the binary representation of the decimal number 42 as
<pre>101010</pre>
This gives us the flag as
<pre>picoCTF{101010}</pre>
Type in the flag and you're done.
