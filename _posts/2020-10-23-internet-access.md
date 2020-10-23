---
layout: post
title: Accessing Internet from command-line
author:  Sabyasachi Ghosh
categories: [SysAdmin]
---

In order to access the internet from the IIT Bombay network, open [https://internet.iitb.ac.in](https://internet.iitb.ac.in) on your browser and login with your IITB LDAP login and password.

Sometimes you may not be able to open a GUI browser such as firefox or chrome, because you've logged in to a lab machine (such as `sl2-11.cse.iitb.ac.in`) via ssh. 
In these cases, do one of the following:

Either, use the command-line browser `lynx` or `links`.
In `lynx`, press `g` and enter `internet.iitb.ac.in`. You can navigate the page using arrow keys.
Enter your username and password and submit, like you'll do on a GUI-based browser.
Or, use the following python3 script:

```python
#!/usr/bin/python3

import requests
import getpass
import sys

ph='10.201.250.201'
ph='internet.iitb.ac.in'

if (len(sys.argv) == 2) and 'logout' == sys.argv[1]:
    r = requests.get('https://'+ ph)
    s = r.content.split('checked="checked"')
    t = s[0].rsplit('value=', 1)
    ip = t[1].strip(' "')
    payload = {'ip':ip, 'button':'Logout'}
    r1 = requests.post('https://' + ph + '/logout.php',
                       cookies=r.cookies, data=payload)
else:
    r = requests.get('https://' + ph + '/index.php')
    payload = {'uname':input('IITB LDAP Username: '),
               'passwd':getpass.getpass()}
    r1 = requests.post('https://' + ph + '/index.php',
                       cookies=r.cookies, data=payload)

```

It will ask you for your IITB LDAP username and password and login.

There is also a python package called `iitb-login`: [https://pypi.org/project/iitb-login/](https://pypi.org/project/iitb-login/).
It saves your password in your home folder (in an encrypted file) the first time you enter it.
Please follow the instructions on the above page to use it.


