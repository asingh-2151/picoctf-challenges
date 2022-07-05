<h1>Warmed Up</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/58">click here</a>
<h2>Overview</h2>
<b>Points</b> - 50<br>
<b>Skills tested</b> - General skills(Hexadecimal to decimal conversion)
<h2>Problem</h2>
What is 0x3D (base 16) in decimal (base 10)?
<h2>Approach</h2>
You can either use a <a href="https://www.rapidtables.com/convert/number/hex-to-decimal.html">hexadecimal-to-decimal conversion calculator</a> or solve this by hand.<br>
<pre>(3D)<sub>16</sub> = ((3X16<sup>1</sup>)+(13X16<sub>0</sub>))<sub>10</sub> = (61)<sub>10</sub>
</pre>
We get the decimal representation of 0x3D as 61.
This gives us the flag as
<pre>picoCTF{61}</pre>
Type in the flag and you're done.
