<h1>Strings it</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/37">click here</a>
<h2>Overview</h2>
<b>Points</b> - 100<br>
<b>Skills tested</b> - General skills(Shell commands)
<h2>Problem</h2>
Can you find the flag in the <a href="https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings">file</a> without running it?
<h2>Approach</h2>
Download the file from  <a href="https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings">here</a>.<br>
(Its good if you have a Linux terminal for this exercise)<br>
<h3>Easy Way Out</h3>
Since they aren't very intent on knowing our way to obtain the flag, you can open the file using <b>Notepad</b> or similar software.<br>
Once inside, <i>Ctrl+F</i> and type in <i>picoCTF</i> to obtain the flag.
<h3>Traditional Way</h3>
Open the terminal, and go to the folder where you have stored the file.<br>
Now type the below commands
<pre>
strings strings | grep picoCTF</pre>
Basically, the <i>strings</i> command sifts out all strings from the file (more than 10,000), and <i>grep</i> searches for the flag in them.<br>
You will get the flag as
<pre>picoCTF{5tRIng5_1T_827aee91}</pre>
Type in the flag and you're done.
