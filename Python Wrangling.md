<h1>Python Wrangling</h1>
Problem link - <a href="https://play.picoctf.org/practice/challenge/166">click here</a>
<h2>Overview</h2>
<b>Points</b> - 10<br>
<b>Skills tested</b> - General skills(Shell/command line and Python3)
<h2>Problem</h2>
<p>Python scripts are invoked kind of like programs in the Terminal... Can you run <a href="https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/ende.py">this Python script</a> using <a href="https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/pw.txt">this password</a> to get <a href="https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/flag.txt.en">the flag</a> ?</p>
<h2>Approach</h2>
Download the python script from <a href="https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/ende.py">here</a>, the password from <a href="https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/pw.txt">here</a>, and the encrypted flag from <a href="https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/flag.txt.en">here</a>.<br>
Enter the terminal and create a directory for executing this flag as
<pre>mkdir pywrangl
cd pywarangl</pre>
While in it, open a python file <i>ende.py</i> using
<pre>nano ende.py</pre>
Once opened the file, copy this code into it (the same code in the original python file)
<pre>
import sys
import base64
from cryptography.fernet import Fernet
usage_msg = "Usage: "+ sys.argv[0] +" (-e/-d) [file]"
help_msg = usage_msg + "\n" +\
        "Examples:\n" +\
        "  To decrypt a file named 'pole.txt', do: " +\
        "'$ python "+ sys.argv[0] +" -d pole.txt'\n"
if len(sys.argv) < 2 or len(sys.argv) > 4:
    print(usage_msg)
    sys.exit(1)
if sys.argv[1] == "-e":
    if len(sys.argv) < 4:
        sim_sala_bim = input("Please enter the password:")
    else:
        sim_sala_bim = sys.argv[3]
    ssb_b64 = base64.b64encode(sim_sala_bim.encode())
    c = Fernet(ssb_b64)
    with open(sys.argv[2], "rb") as f:
        data = f.read()
        data_c = c.encrypt(data)
        sys.stdout.write(data_c.decode())
elif sys.argv[1] == "-d":
    if len(sys.argv) < 4:
        sim_sala_bim = input("Please enter the password:")
    else:
        sim_sala_bim = sys.argv[3]
    ssb_b64 = base64.b64encode(sim_sala_bim.encode())
    c = Fernet(ssb_b64)
    with open(sys.argv[2], "r") as f:
        data = f.read()
        data_c = c.decrypt(data.encode())
        sys.stdout.buffer.write(data_c)
elif sys.argv[1] == "-h" or sys.argv[1] == "--help":
    print(help_msg)
    sys.exit(1)
else:
    print("Unrecognized first argument: "+ sys.argv[1])
    print("Please use '-e', '-d', or '-h'.")
</pre>
Save the file using Ctrl+X key combination.<br>
Now open a text file <i>flag.txt</i> to copy in the encrypted flag.<br>
<pre>nano flag.txt</pre>
Once openend, copy in the encrypted flag
<pre>gAAAAABgUAIWjVP_Ne1VPrHlLZKpvfaifN7qlLoN7NEzOpAl55av7sPuV8wQZj9V-6oI_x4L10O8R-b9c19INaTFrlGbT6YxQeLXd2S3FQA8HmFxU9NILpJGEtVPsGpzPAmLSsRwezRX</pre>
and save the file.<br>
Now type in the below command in the terminal while remaining in the same <i>pywrangl</i> folder
<pre>python3 pywrangl -d flag.txt</pre>
With this command, you aim to decrypt the encrypted flag in the <i>flag.txt</i>file
You will find this displayed on the screen after the execution of the command
<pre>Please enter the password:</pre>
Type in the password
<pre>aa821c16aa821c16aa821c16aa821c16</pre>
and obtain the flag 
<pre>picoCTF{4p0110_1n_7h3_h0us3_aa821c16}}</pre>
Type in the flag and you're done.
