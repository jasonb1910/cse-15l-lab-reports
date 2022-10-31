# Lab Report 3 (Week 5)

In this lab, we will practice with `find` command and some command options of it.

## Using the find command to search files
The general form of the `find` command is:

```find [path] [option] [matching criteria and actions]```

>The `find` command will begin looking in the starting directory you specify and proceed to search through all accessible subdirectories.

Some of the command options we use in this lab: ***-name***, ***-type***, ***-mtime***.

### **-name: : Finding the file by its name**

>You can locate a file by its filename by providing the full file name or parts of the file name using regular expressions

To search files by name in the directory we can use the option `-name`.

For example, we find all text files in *technical* :

`$ find ./technical/911report/ -name "*.txt"`

```
jasonbui@Jasons-MacBook-Air docsearch % find ./technical/911report/ -name "*.txt"
./technical/911report//chapter-13.4.txt
./technical/911report//chapter-13.5.txt
./technical/911report//chapter-13.1.txt
./technical/911report//chapter-13.2.txt
./technical/911report//chapter-13.3.txt
./technical/911report//chapter-3.txt
./technical/911report//chapter-2.txt
./technical/911report//chapter-1.txt
./technical/911report//chapter-5.txt
./technical/911report//chapter-6.txt
./technical/911report//chapter-7.txt
./technical/911report//chapter-9.txt
./technical/911report//chapter-8.txt
./technical/911report//preface.txt
./technical/911report//chapter-12.txt
./technical/911report//chapter-10.txt
./technical/911report//chapter-11.txt
```

We can also find specific file. The find command will search for a filename that is exactly the string we enter between `""` :

`$ find ./technical/911report/ -name "preface.txt"`

```
jasonbui@Jasons-MacBook-Air docsearch % find ./technical/911report/ -name "preface.txt" 
./technical/911report//preface.txt
```

Or, search for all the specific files with matching keywords by using *:

`$ find ./technical/911report/ -name "chapter*"`

```
jasonbui@Jasons-MacBook-Air docsearch % find ./technical/911report/ -name "chapter*"
./technical/911report//chapter-13.4.txt
./technical/911report//chapter-13.5.txt
./technical/911report//chapter-13.1.txt
./technical/911report//chapter-13.2.txt
./technical/911report//chapter-13.3.txt
./technical/911report//chapter-3.txt
./technical/911report//chapter-2.txt
./technical/911report//chapter-1.txt
./technical/911report//chapter-5.txt
./technical/911report//chapter-6.txt
./technical/911report//chapter-7.txt
./technical/911report//chapter-9.txt
./technical/911report//chapter-8.txt
./technical/911report//chapter-12.txt
./technical/911report//chapter-10.txt
./technical/911report//chapter-11.txt
```
### **-type: Finding the file by its type.**

>It's common to optimize the results of find by specifying the file type we're looking for.

The option is `*-type*`, and its arguments are a letter code representing a few different kinds of data. The most common are:

- *d* - directory
- *f* - file
- *l* - symbolic link
- *s* - socket
- *p* - named pipe (used for FIFO)
- *b* - block special (usually a hard drive designation)

For example, we can search for directory of all files in *technical*:

`$ find ./technical/ -type d`

```
jasonbui@Jasons-MacBook-Air docsearch % find ./technical/ -type d         
./technical/
./technical//government
./technical//government/About_LSC
./technical//government/Env_Prot_Agen
./technical//government/Alcohol_Problems
./technical//government/Gen_Account_Office
./technical//government/Post_Rate_Comm
./technical//government/Media
./technical//plos
./technical//biomed
./technical//911report
```

We can also search by file as using file filter in `-type` arguments. This is the list when we run a search that find all files in *911report* (just added 2 more files *Read.java* and *all-java.sh*)

`find ./technical/911report/ -type f `

```
asonbui@Jasons-MacBook-Air docsearch % find ./technical/911report/ -type f
./technical/911report//Read.java
./technical/911report//chapter-13.4.txt
./technical/911report//chapter-13.5.txt
./technical/911report//chapter-13.1.txt
./technical/911report//all-java.sh
./technical/911report//chapter-13.2.txt
./technical/911report//chapter-13.3.txt
./technical/911report//chapter-3.txt
./technical/911report//chapter-2.txt
./technical/911report//chapter-1.txt
./technical/911report//chapter-5.txt
./technical/911report//chapter-6.txt
./technical/911report//chapter-7.txt
./technical/911report//chapter-9.txt
./technical/911report//chapter-8.txt
./technical/911report//preface.txt
./technical/911report//chapter-12.txt
./technical/911report//chapter-10.txt
./technical/911report//chapter-11.txt
```

Searching for the files that named with case-insensitive: 

`$ find ./technical/ -type f -iname "session*"`

```
jasonbui@Jasons-MacBook-Air docsearch % find ./technical/ -type f -iname "session*"
./technical//government/Alcohol_Problems/Session2-PDF.txt
./technical//government/Alcohol_Problems/Session3-PDF.txt
./technical//government/Alcohol_Problems/Session4-PDF.txt
```

### **-mtime: Finding a file modified within a period of time.**

>We can combine -mtime options to locate a file within a range of days

As mentioned above, we added 2 more files *Read.java* and *all-java.sh* to the *911report*. Then, we run the find command `-mtime` to fo find a file we last modified last week:

`$ find ./technical/911report/ -mtime -7`

```
jasonbui@Jasons-MacBook-Air docsearch % find ./technical/911report/ -mtime -7       
./technical/911report/
./technical/911report//Read.java
./technical/911report//all-java.sh
```
We use the `-mtime` option along with a (negative) number of days in the past to find the files that were modified in that period of time.

We can also combine `-mtime` options to locate a file within a range of days. For the first `-mtime` argument, provide the most recent number of days we could have modified the file, and for the second, give the greatest number of days. For instance, this search looks for files with modification times more than one day in the past, but no more than seven:

`$ find ./technical/ -mtime +1 -mtime -7`

```
jasonbui@Jasons-MacBook-Air docsearch % find ./technical/ -mtime +1 -mtime -7
./technical//911report/Read.java
./technical//911report/all-java.sh
```

In this follow-up lab, we have practiced the most important usages of find command with some option examples included ***-name***, ***-type***, and ***-mtime***. The find command makes it convenient for us to save time and find the particular files instantly. If we only know the extension name, its type, or a period of time that the file modified we can still find it by using the find command. 
