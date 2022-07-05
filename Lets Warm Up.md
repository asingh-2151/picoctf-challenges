<h1>Lets Warm Up</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/22">click here</a>
<h2>Overview</h2>
<b>Points</b> - 50<br>
<b>Skills tested</b> - General skills(Hexadecimal to decimal conversion)
<h2>Problem</h2>
If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?
<h2>Approach</h2>
You can either use a <a href="https://www.rapidtables.com/convert/number/hex-to-decimal.html">hexadecimal-to-decimal conversion calculator</a> or solve this by hand.<br>
<pre>(70)<sub>16</sub> = ((7X16<sup>1</sup>)+0)<sub>10</sub> = (112)<sub>10</sub>
</pre>
We get the decimal representation of 0x70 as 112, which can be converted via ASCII system as <b>p</b>
![image](https://user-images.githubusercontent.com/58780673/177251551-92099e8f-97c5-41ed-ade7-e346eb8af978.png)
This gives us the flag as
<pre>picoCTF{p}</pre>
Type in the flag and you're done
