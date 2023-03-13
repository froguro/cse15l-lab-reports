# **Lab Report 5**
For lab report 3, I explored several options for the `find` command.
## `less`
I will be focusing on the `less` command

### **Option 1: `-N`**
Shows line numbers

**Example 1** <br>
```
less -N written_2/non-fiction/OUP/Abernathy/ch1.txt
```
![image](https://cdn.discordapp.com/attachments/776858501720178758/1084623420538490940/image.png)

**Example 2** <br>
```
less -N written_2
```
![image](https://cdn.discordapp.com/attachments/776858501720178758/1084624247319691345/image.png)

### **Option 2: `-X`**
Leaves file content on the screen after exiting `less`

**Example 1** <br>
```
less -X written_2
```
![image](https://user-images.githubusercontent.com/114454864/224581689-ff314506-7aff-4015-badb-9d31b3b71f57.png)

**Example 2** <br>
```
less -X written_2/non-fiction/OUP/Abernathy/ch1.txt
```
![image](https://user-images.githubusercontent.com/114454864/224581785-800dd26a-ac59-4a03-84ad-01698994a368.png)

### **Option 3: `-X`**
Disables clearing the screen when using less

**Example 1** <br>
```
less -pLos written_2/travel_guides/berlitz1/WhatToLosAngeles
```
![image](https://cdn.discordapp.com/attachments/776858501720178758/1084723984643403846/image.png)

**Example 2** <br>
```
less -pWhat written_2/travel_guides/berlitz1/
```
![image](https://cdn.discordapp.com/attachments/776858501720178758/1084725443405557862/image.png)
