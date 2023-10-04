# Lab Report 1 - Hye Won Rhee
1. using `cd`

```
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$ cd lecture1/messages
[user@sahara ~/lecture1/messages]$ cd lecture1/messages/en-us.txt
bash: cd: lecture1/messages/en-us.txt: No such file or directory
```

When the command was run, the directory was lecture1.

The output(s) I got weren't in the form of text but in the directory itself, you can see that even with no argument, the `cd` command changed the directory from lecture1.
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

When the command was run, the directory was just the entire workspace.

The output(s) I got were based on whatever directory I was in/referring to at the time. In the first use of the `ls` command, since the directory is just the workspace as a whole, 
the command listed everything that is in that workspace, which is just the directory lecture1. Whereas when I used a path to a directory as an argument, the command listed out all 
the files in the directory.

Technically the third use of the command seems to be an error because it just reprints the path to the en-us.txt file that I input as an argument. It's an error because the `ls` command
lists out files/folders in folders/directories, not the text/content within files themselves.

3. using `cat`

```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
[user@sahara ~]$ cat lecture1/messages/en-us.txt
Hello World!
[user@sahara ~]$ cat

```

When the command was run, the directory was the entire workspace again.

The first output I got is an error message because the `cat` command prints out the contents of a file or multiple files, not a directory, so using a path to a directory as an argument is
what produced this output. The second output prints the text/contents of the en-us.txt file because the argument referred to the path to a _file_. As for the last output, it is with the same
reasoning as the first use of the command for why it didn't give any output. Using `cd` with no argument is asking it to print the contents of something that is not specified.
