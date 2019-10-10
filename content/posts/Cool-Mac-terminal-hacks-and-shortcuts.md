---
title: Cool Mac terminal hacks and shortcuts
date: '2019-07-17T21:04:17.875Z'
excerpt: >-
  Here is a collection of command line hacks and shortcuts for your Macbook that
  may save you time and make your life easier… some of the…
thumb_img_path: images/Cool-Mac-terminal-hacks-and-shortcuts/1*D4FUSZTV0ZGA4fOGs8GeDA.png
layout: post
---
Here is a collection of command line hacks and shortcuts for your Macbook that may save you time and make your life easier… some of the others are just a bit of fun!

### Make Touch ID your sudo password

If you own or use a Macbook Pro with a Touch Bar you can make your fingerprint your sudo password. To do this:

1.  Open a terminal and edit `/etc/pam.d/sudo`
2.  Add the following line at the top of this file:`auth sufficient pam_tid.so`

![](/images/Cool-Mac-terminal-hacks-and-shortcuts/1*D4FUSZTV0ZGA4fOGs8GeDA.png)

3\. Save the changes.

The next time you need to enter the sudo password you can just use your fingerprint!

![](/images/Cool-Mac-terminal-hacks-and-shortcuts/1*VyPkRZeNg2DKrEaqn0l8Ow.png)

### Enable your mouse cursor in VIM editor

If you want to be able to use your mouse in any file you open in VIM:

1.  Create and edit a new file:`vim ~/.vimrc`
2.  Add this line to the file: `set mouse = a`
3.  Save the file.

You can now use your mouse cursor to navigate and edit different parts of a file while using VIM editor:

![](/images/Cool-Mac-terminal-hacks-and-shortcuts/1*mT3EMD-0Iq1IShBFsTkdYg.gif)

### Converting Unix Epoch time

Previously whenever I wanted to convert Unix Epoch time to human-readable time, I always used [https://www.epochconverter.com](https://www.epochconverter.com/). It’s actually quite embarrassing how often I used this site until I discovered you can simply run `date -r` followed by the Epoch timestamp from the command line.

![](/images/Cool-Mac-terminal-hacks-and-shortcuts/1*l9uRJrNf8FmmicZpNcVFxw.png)

### Get your Macbook to speak

Type “say” following by text and your Macbook reads it out.

![](/images/Cool-Mac-terminal-hacks-and-shortcuts/1*JUT4vhEpgIAo63Gqmzjgaw.png)

<figcaption>For fans of <a href="https://en.wikiquote.org/wiki/2001:_A_Space_Odyssey_%28film%29" data-href="https://en.wikiquote.org/wiki/2001:_A_Space_Odyssey_(film)" class="markup--anchor markup--figure-anchor" rel="noopener" target="_blank">2001: A Space&nbsp;Odyssey</a>…</figcaption>

If you want to see a list of all of the available voice options in the Mac OS version you have installed, run this command: `say -v '?'`

### Stop your Macbook from falling asleep

You can stop your Macbook from falling asleep using `caffeinate` followed by the time in seconds you want your laptop to stay awake for:

    caffeinate -t 6000

### View all previous commands

Use `history` to view all previous commands you have run from the terminal.

Or if you don’t want anyone to see what commands you’ve run previously, you can delete your command history using:

    history -c 

### Get the weather forecast

You can send a cURL request to retrieve the current weather forecast. Type the following command: `curl [http://wttr.in/](http://wttr.in/) <your_city_name>` .

For example, `curl [http://wttr.in/](http://wttr.in/) london` returns the following:

![](/images/Cool-Mac-terminal-hacks-and-shortcuts/1*gdFvYh0_Zi8L28_9bFYTuw.png)

### Play Games

If you simply want to play some old school games from your terminal:

1.  Open your terminal and run`emacs`
2.  Press **Enter** followed by **Esc**.
3.  Type ‘x’ and enter the name of the game you want to play such as ‘tetris’:

![](/images/Cool-Mac-terminal-hacks-and-shortcuts/1*BWi0oGpk28M-ZkrwzVOVuQ.png)

4\. Other valid options include: ‘snake’, ‘pong’, ‘doctor’, ‘landmark’, ‘gomoku’, ‘dunner’ or ‘solitaire’ (the marble game, not the card game!)

Have fun!
