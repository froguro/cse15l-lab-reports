# **Lab Report 5**
For lab report 3, I explored several options for the `find` command.
## `less`
I will be focusing on the `less` command

### **Option 1: `-N`**
Shows line numbers <br>
[Source](https://phoenixnap.com/kb/less-command-in-linux)

**Example 1** <br>
```
less -N written_2/non-fiction/OUP/Abernathy/ch1.txt
```
![image](https://cdn.discordapp.com/attachments/776858501720178758/1084623420538490940/image.png)

Here you can see that in the less window, there are now line numbers on the left-hand side. This is very useful to use as a reference point when viewing files.

**Example 2** <br>
```
less -N written_2
```
![image](https://cdn.discordapp.com/attachments/776858501720178758/1084624247319691345/image.png)

This can also be used on directories. Probabably not as useful as when used for text files but it works.

### **Option 2: `-X`**
Leaves file content on the screen after exiting `less` <br>
[Source](https://phoenixnap.com/kb/less-command-in-linux)
**Example 1** <br>
```
less -X written_2
```
![image](https://user-images.githubusercontent.com/114454864/224581689-ff314506-7aff-4015-badb-9d31b3b71f57.png)

As you can see, the contents of less remains in the terminal after exiting. This is useful for when you want to continue running commands but you need to remember what was in less.

**Example 2** <br>
```
less -X written_2/non-fiction/OUP/Abernathy/ch1.txt
```
![image](https://user-images.githubusercontent.com/114454864/224581785-800dd26a-ac59-4a03-84ad-01698994a368.png)

Here is the same command used on a fairly large text file. It will fill up a good chunk of the screen and kind of takes away from the convenience of less' uncluttered default setting.

### **Option 3: `-p[pattern]`**
Searches for a certain pattern <br>
[Source](https://phoenixnap.com/kb/less-command-in-linux)

**Example 1** <br>
```
less -pLos written_2/travel_guides/berlitz1/WhatToLosAngeles
```
![image](https://cdn.discordapp.com/attachments/776858501720178758/1084723984643403846/image.png)

When used on a text file, the certain string that you inputted will be highlighted if it exists. This is useful to look for a certain part of a text file without having to type the command out after you open the less window.

**Example 2** <br>
```
less -pWhat written_2/travel_guides/berlitz1/
```
![image](https://cdn.discordapp.com/attachments/776858501720178758/1084725443405557862/image.png)

The same can be done on a directory. This could be useful for directories with many files.

### **Option 4: Viewing multiple files through less **

You can view multiple files through one command by simply putting the file names one after another. <br>
To traverse through the list of files you inputted, you can use `:n` for next and `:p` for previous. <br>
[Source](https://linuxhandbook.com/less-command/)
**Example 1** <br>
```
less WhatToLosAngeles.txt WhatToLasVegas.txt
```
You can use less to view multiple text files. Upon opening, you will view the first text file inputted. Pressing `:n` will allow you to view the next. This is a useful thing if you were planning to view multiple files. You would not have to rewrite the command. 

**Example 2** <br>
```
less non-fiction/ travel_guides/
```
This can also be done on directories. This is useful if you happen to want to see multiple directories using less.
