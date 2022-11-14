# Lab Report 4 (Week 7)

In this lab, we will practice editing from the command line by using vim editor.

## Part 1 ##

**Task:** *Changing the name of the `start` parameter and its uses to `base`*

First of all, we need to clone the repository from `skill-demo1` and put it in the `week7-skill-demo`

`$ git clone https://github.com/ucsd-cse15l-f22/skill-demo1 week7-skill-demo`

From "week7-skill-demo" directory, we start to edit "DocSearchServer.java" in `vim`

We use the command line `vim DocSerchServer.java<Enter>` to open file "DocSearchServer.java" in vim. 

![image]()

Then, this is how the "DocSearchServer.java" looks like in vim.

![image]()

`/start<Enter>`: the command line that we search for the keyword "start" that need to be changed.

![image]()

`cebase`: the command line that switching into input mode and deleting the word "start", then relacing with word "base". `<Esc>` to exit input mode.

![image]()

`n`: the command line that going to the next found word. Then `.` to copy from the last modification.

![image]()

After changing all the words "start" to "base", we use the command line `:wq` to save and exit vim.

![image]()

This is the sequence that we use for the task:

`vim DocSearchServer.java<Enter>/start<Enter>cebase<Esc>n.n.n.:wq<Enter>`


