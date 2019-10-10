---
title: A bitesize intro to Unix (with pixel art)
date: '2019-03-04T07:01:00.754Z'
excerpt: >-
  While it might not be everyone’s cup of tea, Unix is an incredibly useful
  operating system to learn. Unix is under the hood of everything…
thumb_img_path: images/A-bitesize-intro-to-Unix--with-pixel-art/1*1UGV88CRCnsy4_JVvqzqAg.jpeg
layout: post
---
![](/images/A-bitesize-intro-to-Unix--with-pixel-art/1*1UGV88CRCnsy4_JVvqzqAg.jpeg)

While it might not be everyone’s cup of tea, Unix command line is incredibly useful to learn. Unix-based operating systems are under the hood of everything from Android phones to Chromebooks, Macbooks and even Playstations so there’s a pretty high chance you have used a \*nix-powered device at some point in your life.

Learning Unix command line offers you a quick and powerful way to carry out tasks like file management, troubleshooting and customisation. Plus the next time you watch Mr Robot you might actually be able to understand some of what Elliot is typing!

Inspired by the covers of [Julia Evans](https://medium.com/u/152f65dab15)’ programming [zines](https://wizardzines.com/), I’ve created a tutorial to explain most of the commonly-used Unix commands, along with some accompanying pixel art — specially designed for people who don’t want to make a meal out of learning Unix 😉.

### Entrée — Listing files and directories.

To start using Unix, it’s important to know how to navigate your way around your file system and its various directories:

![](/images/A-bitesize-intro-to-Unix--with-pixel-art/1*2R-DyNb8bqLIgHFlaIpFFQ.png)

`**ls**` (list segments — like a lemon!) — lists the files and directories in your current working directory. You can use different options with `**ls**` to sort or display additional information:

*   `**ls -l**`: displays files + permissions, owner, group, size, time and name.
*   `**ls -t**`: sorts files by time.
*   `**ls -r**`: sorts files in reverse order.

`**cd**` (change directory) — change your current working directory to another folder. You can specify the file path you want to move to as follows:

    **cd /usr/folder/subfolder**

You can go back to the previous directory with `**cd -**`or move up one folder with:`**cd ..**`  or move up three folders with `**cd ../../..**`

`**pwd**` (print working directory) — displays the path of the current working directory you are in. Not really used for much else, just a good way to find out where on earth you are if you get lost!

`**mkdir**` (make directory) — creates a directory if it does not already exist. For example, to create a directory called “stuff”:

    **mkdir stuff**

You can also make subdirectories using the `-p` option:

    **mkdir -p /home/stuff/morestuff**

You can also use `**rmdir**` to remove a directory.

### Starter — File operations

The next things to familiarise yourself with are copying, moving, creating and removing things:

![](/images/A-bitesize-intro-to-Unix--with-pixel-art/1*Q_J1DrB3P5u3ky5Z05dMOw.png)

`**cp**` (copy) — creates a duplicate of file or directory. To use it, enter `**cp**` followed by the source file and the new file name:

    **cp myfile1.txt myfile2.txt**

Alternatively enter the source file name and location you want to create a copy in. For example:

    **cp myfile.txt /Users/your.name/Documents**

`**mv**`(move) — move one or more files or directories from one location to another. Like `**cp**` it follows the format, `**mv sourcefile destination**`. For example:

    **mv ~/Desktop/myfile.text ~/MyFolder**

`**touch**`— a quick way to create a file or multiples files. You can also use `**touch**` to change a file’s timestamp. Pass the name of the file you want to create as follows:

    **touch filename.text**

If a file already exists with that name, `**touch**` updates the file’s access time (last time it was read), modification time (last time the contents were modified) and change time (last time the file’s metadata was changed).

`**rm**` (remove) — delete files. Enter the command and the file’s location:

    **rm /home/Desktop/-file.txt**

Be warned `**rm**` can be quite a dangerous command to use if you don’t know what you’re doing. The one to really avoid is the dreaded `**rm -rf /**` which essentially deletes every file in your Unix system. Linux blogger Wayne Richardson posted a video of what happens if you run it if you’re curious:

<iframe src="https://www.youtube.com/embed/D4fzInlyYQo?feature=oembed" width="640" height="480" frameborder="0" scrolling="no"></iframe>

### Main — File searching, permissions and ownership.

You can search for files and directories and change the permissions and ownership for different files and directories:

![](/images/A-bitesize-intro-to-Unix--with-pixel-art/1*E9ntSdHMWgXJbPGTFv3tbw.png)

`**find**` — find files and directories in your system. For example:

    **find ./directoryname -name file.txt**

You can also find all files with a certain pattern. For example, all files that end .txt:

    **find ./directoryname -name *.txt**

`**grep**` (global regular expression print) — search for text or search within a specified file for text matching a given string. You can couple it with the `-i` to make case insensitive searches:

    **$grep -i "grape" wine.txt**

This would return:

    **Grape** varieties includes cultivated **grape**, whether used for wine, or eating as a table **grape**, fresh or dried (raisin, currant, sultana). The term **grape** probably comes from *graper* from a Frankish or other Germanic word for "hook".

You can also use `**grep**` to count the number of times a word appears in a file:

    **$grep -c "grape" wine.txt**

For this file the output would be `**4**`.

`**chmod**`(change mode) — changes the permissions for files and directories. There are three classes you define permissions for: Owner (the owner of the file), Group (users of the same group) and Others (anyone else). You enter one of the following numbers for each class when you run chmod:

0 — No permission.  
1 — Execute.  
2 — Write.  
3 — Write and execute.  
4 — Read.  
5 — Read and execute.  
6 — Read and write.  
7 — Read, write, and execute.

For example, `**chmod 777**` grants read, write and execute permissions to all classes and `**chmod 755**` grants all permissions to the owner of the file but only read and execute permissions to other users.

`**chown**`(change owner) — changes ownership of files and directories in your file system. To change the owner of a text file:

    **sudo chown myuser myfile.txt**

### Extras — Comparing, linking, tailing and killing.

You can compare files, link files, output the tail of files and kill processes:

![](/images/A-bitesize-intro-to-Unix--with-pixel-art/1*u_DVAeOL7OzYniVpEj10Fw.png)

<figcaption>Campino (cmp) were a strawberry candy sold in the UK. Now discontinued.</figcaption>

`**cmp**` — Compare the bytes between different files. If there are no differences between the two files, no output is returned. The format for using `**cmp**` is:

    **cmp -b textfile1.txt textfile2.txt**

The output for files with several differences is:

    **textfile1.txt textfile2.txt differ: byte 20, line 1 is  56 . 162 r**

`**cat**`(concatenate) — use it to create a file, link multiple files together or display the contents of a file. For example, to link or “concatenate” two text files (file1.txt and file2.txt) to create new text file:

    **cat file1.txt file2.txt > file3.txt**

`**tail**` — output the “tail”, the final part, of a file. By default tail outputs the last 10 lines of a file. You can use `tail` as follows:

    **tail textfile.txt**

To output a greater number of lines, you can use the `**-n**` option:

    **tail -n 50 textfile.txt**

`**kill**` — terminates a process. To see the signals you can kill run: `**kill -l**`. You can terminate a specific process as follows:

    **kill -s signalName PID**

### Desserts — More, Curl, SSH and Sudo.

Some additional commands you can use in Unix include `more`, cURL, SSH and Sudo:

![](/images/A-bitesize-intro-to-Unix--with-pixel-art/1*uXsxGG-GrID1QNJH2hPNkA.png)

`**more**` — display more text on the screen. To use`**more**` to display the contents of a file beginning at line 10:

    **more +10 myfile.txt**

`**curl**` (Client URL) — a command line tool for transferring data over various protocols (HTTP, SMTP, LDAP, SCP etc). This comes in-built with MacOS and most Linux-based operating systems.

You can use cURL to send data or retrieve data over HTTP using an API request. For example, if you set up a webhook with Slack, you can use cURL to send a message to a Slack channel:

    **curl -X POST -H 'Content-type: application/json' --data '{"text":"Good morning everyone!"}' your_webhook_url**

`**ssh**` (Secure Shell) — use it to operate securely over an unsecured network. The syntax for using `**ssh**` to login to a remote host is as follows:

    **ssh remote_host**

Alternatively to `**ssh**` into the remote host as a root user. For example, this might be useful if you wanted to edit configuration files on a system in a virtual machine:

    **ssh root@remote_host**

`**sudo**`  (superuser do) — allows you to execute commands as a superuser. You can use `**sudo**` if you know the root password for your Unix system. For example to shutdown your machine using `**sudo**`:

    **sudo shutdown -r now**

### Drinks — Text editors.

There a number of core text editors you can use in Unix-based operating systems:

![](/images/A-bitesize-intro-to-Unix--with-pixel-art/1*vDGteZVZgRuhtdkuUtxO0w.png)

<figcaption>Note for non-British readers: Vimto is an amazing grape/berry soft drink in the UK&nbsp;:)</figcaption>

`**vi**`— the original text editor created for Unix by developer [Bill Joy](https://en.wikipedia.org/wiki/Bill_Joy). Despite being released way back in 1976 it is still one of the most popular text editors for Linux-based systems.

`**vim**` (short for Vi Improved) — is a clone of the original Vi editor. Enhancements with Vim are the inclusion of plugins, the comparison and merging of files, and the ability to edit compressed files in formats such as gzip, zip and tar.

`**emacs**` (Editor MACroS) — another old-timer of a text editor. Like Vi, it was also released in 1976 and is one of the oldest open source projects still in development.

One cool tip if you launch Emacs is if you press **Esc**, type **x** and type **pong**, it launches a game of pong:

![](/images/A-bitesize-intro-to-Unix--with-pixel-art/1*qZR1MRKMp2CiaSk_fhiKqg.png)

This also works for **tetris**, **snake**, and **solitaire** (the marble game not the card game!).

`**nano**` — another editor for Unix-like operating systems. Initially released in June 2000, GNU nano is a simple text editor that’s very beginner friendly.

You can also use open-source text editors like Atom or Sublime if you prefer. These come with way more bells and whistles (things like linters to check there are no syntax or stylistic errors in your code). Hopefully some of this tutorial was useful. Good luck on your \*nix adventures and remember to be careful with `rm`!

**Note**: Here is the full “[menu](https://ibb.co/vzNvPxZ)” of pixel art if you want to download it.
