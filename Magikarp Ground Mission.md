<h1>Magikarp Ground Mission</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/189">click here</a>
<h2>Overview</h2>
<b>Points</b> - 30<br>
<b>Skills tested</b> - General skills(Shell/command line)
<h2>Problem</h2>
<p>Do you know how to move between directories and read files in the shell? Start the container, <i>ssh</i> to it, and then <i>ls</i> once connected to begin. Login via <i>ssh</i> as <b>ctf-player</b> with the password, <b>6d448c9c</b></p>
<h2>Approach</h2>
Begin by connecting to the server using
<pre>ssh ctf-player@venus.picoctf.net -p 51329</pre>
and password
<pre>6d448c9c</pre>
<b>Note</b> - The last 5 digits in the ssh access key will vary across each instance launched<br>
Using <i>ls</i>, we get
<pre>1of3.flag.txt  instructions-to-2of3.txt</pre>
Now open <i>1of3.flag.txt</i> using
<pre>cat 1of3.flag.txt</pre>
to get the first part of the key i.e.
<pre>picoCTF{xxsh_</pre>
Now open the <i>instructions-to-2of3.txt</i> using
<pre>cat instructions-to-2of3.flag.txt</pre>
where you will see
<pre>Next, go to the root of all things, more succinctly `/`</pre>
Now type in the below commands
<pre>cd<br>ls -a</pre>
You will see a list of files as displayed below
<pre>.  ..  .cache  .profile  .ssh  3of3.flag.txt  drop-in</pre>
Now access <i>3of3.flag.txt</i> using
<pre>cat 3of3.flag.txt</pre>
to get the third part of the key i.e.
<pre>5190b070}</pre>
All that remains now is the second part of the key. While there must be multiple ways to access copies of <i>2of3.flag.txt</i>, here is the easiest method to do so.
Type in the below commands once
<pre>cd ..<br>ls -a</pre>
You will see this displayed on the screen
<pre>.  ..  ctf-player</pre>
Again type in the below commands
<pre>cd ..<br>ls -a</pre>
And you will see this on the screen
<pre>.  ..  .dockerenv  2of3.flag.txt  bin  boot  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var</pre>
For those who didn't understand, basically I went into the .. directory, which had a .. directory which contained <i>2of3.flag.txt</i><br>
Having reached <i>2of3.flag.txt</i>, all that remains is to access it using
<pre>cat 2of3.flag.txt</pre>
To obtain the second and the final part of the flag i.e.
<pre>0ut_0f_\/\/4t3r_</pre>
With this, we obtain the flag
<pre>picoCTF{xxsh_0ut_0f_\/\/4t3r_5190b070}</pre>
Type in the flag and you're done.
