# Lab Report 4 (Week 7)

In this lab, we will practice editing from the command line by using Vim Editor.

## Part 1

**Task:** *Changing the name of the `start` parameter and its uses to `base`*

First of all, we need to clone the repository from `skill-demo1` and put it in the `week7-skill-demo`

`$ git clone https://github.com/ucsd-cse15l-f22/skill-demo1 week7-skill-demo`

From "week7-skill-demo" directory, we start to edit "DocSearchServer.java" in Vim

We use the command line `vim DocSerchServer.java<Enter>` to open file "DocSearchServer.java" in Vim. 

![image](Screenshot 2022-11-13 at 5.02.44 PM.png)

Then, this is how the "DocSearchServer.java" looks like in Vim.

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

Following the edit task we chose, there are two ways that we can use for it:

- [Option 1] Start in Visual Studio Code and make the edit there, then use `scp` coping the updated file to the remote server and run it on the remote.
- [Option 2] Start directly on remote server and make the edit in Vim, then run it on the remote.

After timing the process from the beginning, we ended up with :

| Option 1 | Option 2 |
| approx. 6 mins | approx. 5 mins |



