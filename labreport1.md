# Lab Report 1 - Hye Won Rhee
1. using `cd`

```
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$ cd lecture1/messages
[user@sahara ~/lecture1/messages]$ cd lecture1/messages/en-us.txt
bash: cd: lecture1/messages/en-us.txt: No such file or directory
```

When the command was run, the directory was lecture1.

Since we used the `cd` command with no arguments, the working directory was returned to the home directory. 
As for the third use of the command, which had a path to a file as an argument, there is the message "No such file or directory", because since it is a path to a file, technically the directory cannot be changed.

2. using `ls`

```
[user@sahara ~]$ ls
lecture1
[user@sahara ~]$ ls lecture1/messages
en-us.txt  es-mx.txt  zh-cn.txt
[user@sahara ~]$ ls lecture1/messages/en-us.txt
lecture1/messages/en-us.txt
```

The working directory when the command was run was the home directory, as marked with the tilde(~).

The output(s) I got were based on whatever directory I was in/referring to at the time. In the first use of the `ls` command, since the directory is just the workspace as a whole, 
the command listed everything that is in that workspace, which is just the directory lecture1. Whereas when I used a path to a directory as an argument, the command listed out all 
the files in the directory.

The third use of the command isn't an error. Instead, using the `ls` command with the argument `lecture1/messages/en-us.txt` simply lists the files given in the file argument.

3. using `cat`

```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
[user@sahara ~]$ cat lecture1/messages/en-us.txt
Hello World!
[user@sahara ~]$ cat
lecture1/messages/en-us.txt
lecture1/messages/en-us.txt
```

When the command was run, the directory was the home directory once again.

The first output I got is an error message because the `cat` command prints out the contents of a file or multiple files, not a directory, so using a path to a directory as an argument is
what produced this output. The second output prints the text/contents of the en-us.txt file because the argument referred to the path to a _file_. As for the last output, using the `cat` command with no args causes it to read its standard input as nothing and thus stays in the terminal. However, if a user were to type something after using the command this way and hit enter, `cat` will read from its standard input and produce it as its standard output. 
