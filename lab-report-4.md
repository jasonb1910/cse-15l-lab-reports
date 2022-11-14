# Lab Report 4 (Week 7)

In this lab, we will practice editing from the command line by using vim editor.

## Part 1

**Task:** *Changing the name of the `start` parameter and its uses to `base`*

First of all, we need to clone the repository from `skill-demo1` and put it in the `week7-skill-demo`

`$ git clone https://github.com/ucsd-cse15l-f22/skill-demo1 week7-skill-demo`

From "week7-skill-demo" directory, we start to edit "DocSearchServer.java" in `vim`

We use the command line `vim DocSerchServer.java<Enter>` to open file "DocSearchServer.java" in vim. 

![image](Screenshot 2022-11-13 at 5.02.44 PM.png)

Then, this is how the "DocSearchServer.java" looks like in vim.

![image](Screenshot 2022-11-13 at 5.28.15 PM.png)

`/start<Enter>`: the command line that we search for the keyword "start" that need to be changed.

![image](Screenshot 2022-11-13 at 5.32.55 PM.png)

`ce`: the command line that switching into input mode and deleting the word "start".

![image](Screenshot 2022-11-13 at 5.32.15 PM.png)

`base` to relace with word "base".

![image](Screenshot 2022-11-13 at 5.32.36 PM.png)

Then, `<Esc>` to exit input mode.

`n`: the command line that going to the next found word.

![image](Screenshot 2022-11-13 at 5.32.55 PM.png)

Using `.` to input from the copy of our last modification.

![image](Screenshot 2022-11-13 at 5.33.01 PM.png)

After changing all the words "start" to "base", we use the command line `:wq<Enter>` to save and exit vim.

![image](Screenshot 2022-11-13 at 5.36.39 PM.png)

There are a lot of ways that we can use to edit this task. One of those is represented above and we can come up with the sequence like this after all:

`vim DocSearchServer.java<Enter>/start<Enter>cebase<Esc>n.n.n.:wq<Enter>`

## Part 2


