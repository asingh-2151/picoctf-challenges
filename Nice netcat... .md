<h1>Nice netcat...</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/156">click here</a>
<h2>Overview</h2>
<b>Points</b> - 15<br>
<b>Skills tested</b> - General skills(Shell/command line + Netcat)
<h2>Problem</h2>
There is a nice program that you can talk to by using this command in a shell: <i>$ nc mercury.picoctf.net 43239</i>, but it doesn't speak English...
<h2>Approach</h2>
Begin by connecting to the server using
<pre> nc mercury.picoctf.net 43239</pre>
On executing the command, you will get a list of numbers
<pre>112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
55 
99 
48 
56 
50 
49 
102 
53 
125 
10</pre>
It is quite evident from here that these are basically the ASCII representation of each character in the flag.
Use any programming language you want, run the array through it and convert back each character using its ASCII number to get the flag. Here's my python code for reference
<pre>s=""
for i in arr:
    s+=chr(i)
print(s)</pre>
On executing this code, you will obtain the flag
<pre>picoCTF{g00d_k1tty!_n1c3_k1tty!_7c0821f5}</pre>
Type in the flag and you're done.
