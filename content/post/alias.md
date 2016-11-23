+++
Categories = []
Description = ""
Subtitle = ""
Tags = ["tech"]
date = "2016-11-23T15:19:11-05:00"
draft = "false"
slug = ""
title = "How to Create an Alias for the Command Line"

+++

If you use a Linux-style terminal you may find yourself typing the same commands over and over again. If this is the case, you may wish to use some shorthand that the terminal can understand. You can do that with Aliases.

You start by going to your user directory and opening your <code>.bashrc</code> file. A <code>.bashrc</code> is a shell script that [Bash](https://en.wikipedia.org/wiki/Bash_(Unix_shell\)) runs whenever it is started interactively. You can put any command in that file that you could type at the command prompt. 

In my case, I wanted to avoid having to type "git push origin master" every time I wanted to commit changes to my remote repository, so I appended the following line of code to my <code>.bashrc</code> file:

<code>alias gpom='git push origin master'</code>

and saved the file.

Now, whenever I have something to commit I just type: 'gpom' and press enter.

**Note**: In order for the new alias to work you have to reboot your computer.


