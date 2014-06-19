za.github.io
============

The [za.github.io](http://za.github.io) source code. 

Question:
* [Q] How to automatically update with SSH-key without have to type SSH-key password?
* [A] Try to use ``ssh-agent`` 
* Still need to type password

Run: 

``$ ssh-agent``

``$ ssh-add``

  Enter passphrase for /home/za/.ssh/id_rsa:
  Identity added: /home/za/.ssh/id_rsa (/home/za/.ssh/id_rsa)
