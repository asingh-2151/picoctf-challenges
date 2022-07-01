<h1>First Find</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/320">click here</a>
<h2>Overview</h2>
<b>Points</b> - 100<br>
<b>Skills tested</b> - General skills(Unzipping archives)
<h2>Problem</h2>
<p>Unzip <a href="https://artifacts.picoctf.net/c/551/files.zip">this</a> archive and find the file named <i>uber-secret.txt</i></p>
<h2>Approach</h2>
Download the <i>.zip</i> file from the link given  <a href="https://artifacts.picoctf.net/c/551/files.zip">here</a>.<br>
Extract the unzipped version of the archive which will be stored in your system under the name <i>files</i>.<br>
On entering the folder, you will find
<pre>files</pre>
Enter this <i>files</i> folder to find
<pre>acceptable_books adequate_books satisfactory_books 13771.txt.utf-8 14789.txt.utf-8</pre>
Enter the folder <i>adequate_books</i> to find
<pre>more_books 44578.txt.utf-8 46804-0</pre>
Enter the folder <i>more_books</i> to find
<pre>.secret 1023.txt.utf-8</pre>
Enter the folder <i>.secret</i> to find
<pre>deeper_secrets</pre>
Enter the folder <i>deeper_secrets</i> to find
<pre>deepest_secrets</pre>
Enter the folder <i>deepest_secrets</i> to find
<pre>uber_secret.txt</i>
With this, we obtain the flag
<pre>picoCTF{f1nd_15_f457_ab443fd1}</pre>
Type in the flag and you are done.
