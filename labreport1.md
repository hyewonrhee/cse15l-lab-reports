# Lab Report 1
*How to Log Into a Course-Specific Account on* `ieng6`:

**Step 1:** Installing VScode

  For this step, I already had VScode installed from a previous course. However,
  there was no option to select the default profile of `bash` or `zsh`. But with
  support from the TAs, I was able to pinpoint the problem, which was the fact that my
  version of VScode was not up to date.
  
  ![Image](LRstep1.jpg)
  
  To solve a similar problem, click the settings button on the bottom-left corner and click "Check for
  Updates". VScode will then close to restart, and you will need to open the application again.
  
  If you do not have VSCode applied yet, click on the link: https://code.visualstudio.com/ and follow the
  specific directions for your type of computer (Windows, Mac, etc).
  
**Step 2:** Remotely Connecting

  To open a new terminal in VScode, at the very top click Terminal and then New Terminal.
  ![Image](LRstep2.png)
  
  Next, select the arrow pointing downwards next to the + sign, and select either `zsh` or `bash`.
  ![Image](LRstep2.2.png)
  
  Now you're ready to log into your course-specific account.
  
  To login, type in `ssh` and then your course-specific username, ending in `@ieng6.ucsd.edu`.
  
  Your command should look like this:
  
  `$ ssh cs15lsp23ql@ieng6.ucsd.edu`
  
  Then it will ask you for your password, which will not appear as you type it in for security reasons.
  
  Then once it logs into the remote server, it should look something like this:
  
  ![Image](LRstep2.3.png)
  
  In this specific instance, the password-change tool was not working for some time before I finally
  was able to successfully login, and the output shows exactly that by saying the time and date of
  the `Last failed login:`.
  
**Step 3:** Trying Some Commands

  Now it's time to try some commands! 
  
  Using commands such as `cp`, `pwd`, `cd`, `ls`, or `mkdir`, test these out using both the remote
  server and your own computer.
  
  (`cp` copies a file from one place to another)
  
  (`pwd` prints the name of the current working directory)
  
  (`cd` changes the current working directory)
  
  (`ls` lists the files in your current directory)
  
  (`mkdir` creates a new directory)
  
  Example tests using these commands should look something like this:
  
  ![Image](LRstep3.png)
  
  In this specific instance, since I was using the remote server, when I typed in the command
  `cd /Users/`, I was attempting to change the directory into /Users/, but it gave me the message that
  there is no such file or directory, since I had specified a directory that is only on my own computer.
  
  As for the `ls <directory>` command, I had used the `ls` command to list out the files but did not specify
  which directory I wished the to see the files of. 
