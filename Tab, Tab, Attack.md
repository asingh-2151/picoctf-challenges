<h1>Lets Warm Up</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/176">click here</a>
<h2>Overview</h2>
<b>Points</b> - 20<br>
<b>Skills tested</b> - General skills(Shell commands/opening files)
<h2>Problem</h2>
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames:<a href="https://mercury.picoctf.net/static/659efd595171e4c40378be6a2e9b7298/Addadshashanammu.zip">Addadshashanammu.zip</a>
<h2>Approach</h2>
Download the file from <a href="https://mercury.picoctf.net/static/659efd595171e4c40378be6a2e9b7298/Addadshashanammu.zip">here</a>/<br>
Unzip the file as a folder <i>Addadshashanammu</i><br>
Assuming that the entire unzipped folder is in a folder X, execute the commands
<pre>cd \Addadshashanammu
ls</pre>
You will see on the screen
<pre>Almurbalarammi</pre>
which is a folder.<br>
Now execute the below two commands
<pre>cd \Addadshashanammu\Almurbalarammi
ls</pre>
You will see on the screen
<pre>Ashalmimilkala</pre>
which is a folder.<br>
Now execute the below two commands
<pre>cd \Addadshashanammu\Almurbalarammi\Ashalmimilkala
ls</pre>
You will see on the screen
<pre>Assurnabitashpi</pre>
which is a folder.<br>
Now execute the below two commands
<pre>cd \Addadshashanammu\Almurbalarammi\Ashalmimilkala\Assurnabitashpi
ls</pre>
You will see on the screen
<pre>Maelkashishi</pre>
which is a folder.<br>
Now execute the below two commands
<pre>cd \Addadshashanammu\Almurbalarammi\Ashalmimilkala\Assurnabitashpi\Maelkashishi
ls</pre>
You will see on the screen
<pre>Onnissiralis</pre>
which is a folder.<br>
Now execute the below two commands
<pre>cd \Addadshashanammu\Almurbalarammi\Ashalmimilkala\Assurnabitashpi\Maelkashishi\Onnissiralis
ls</pre>
You will see on the screen
<pre>Ularradallaku</pre>
which is a folder.<br>
Now execute the below two commands
<pre>cd \Addadshashanammu\Almurbalarammi\Ashalmimilkala\Assurnabitashpi\Maelkashishi\Onnissiralis\Ularradallaku
ls</pre>
You will see on the screen
<pre>fang-of-haynekhtnamet</pre>
Which is the file you have to work with.
<h3>Easy Way Out</h3>
Since they aren't very intent on knowing our way to obtain the flag, you can open the file using <b>Notepad</b> or similar software.<br>
Once inside, <i>Ctrl+F</i> and type in <i>picoCTF</i> to obtain the flag.
<h3>Traditional Way</h3>
Open the terminal, and go to the folder where you have stored the file.<br>
Now type the below commands
<pre>
strings fang-of-haynekhtnamet | grep picoCTF</pre>
Basically, the <i>strings</i> command sifts out all strings from the file (more than 10,000), and <i>grep</i> searches for the flag in them.<br>
<pre>picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4}</pre>
Type in the flag and you're done.
