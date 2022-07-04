<h1>What's a net cat?</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/34">click here</a>
<h2>Overview</h2>
<b>Points</b> - 100<br>
<b>Skills tested</b> - General skills(Shell/command line + Netcat)
<h2>Problem</h2>
Using netcat (nc) is going to be pretty important. Can you connect to <i>jupiter.challenges.picoctf.org</i> at port <i>64287</i> to get the flag?
<h2>Approach</h2>
Begin by connecting to the server using
<pre>nc jupiter.challenges.picoctf.org 64287</pre>
<b>Note</b> - The last 5 digits in the access key will vary across each instance launched<br>
On executing the command, you will get a congratulatory message and the flag
<pre>You're on your way to becoming the net cat master
picoCTF{nEtCat_Mast3ry_284be8f7}</pre>
Type in the flag and you're done.
