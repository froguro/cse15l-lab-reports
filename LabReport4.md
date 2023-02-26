# **Lab Report 4**

## Steps

### Log into ieng6

![image](https://cdn.discordapp.com/attachments/776858501720178758/1079533945978376233/image.png) <br/>
Keys pressed: ssh`<space>`cs15lwi23axq@ieng6.ucsd.edu <br/>
*sshing into ieng6 as normal*
### Clone your fork of the repository from your Github account

![image2](https://cdn.discordapp.com/attachments/776858501720178758/1079534332898705458/image.png) <br/>
Keys pressed: `<ctrl-r>`git`<space>`clone`<enter>` <br/>
*Since `git clone git@github.com:froguro/lab7.git` was already in my command history, I can search for it using `<ctrl-r>` and the correct line is autofilled after I  type `git clone`.*

### Run the tests, demonstrating that they fail

![image3](https://cdn.discordapp.com/attachments/776858501720178758/1079535014133379183/image.png) <br/>
Keys pressed: cd`<space>`lab7`<enter><ctrl-r>`javac`<enter><ctrl-r>`java`<space><enter>` <br/>
*First, I simply changed directory to `lab7`. Then I used `<ctrl-r>` to search for `javac` which autofills to the command to compile and then I use`<ctrl-r>` again to search for `java` which autofills to my command to run the tests.*

### Edit the code file to fix the failing test

![image4](https://cdn.discordapp.com/attachments/776858501720178758/1079537414936215602/image.png) <br/>
Keys pressed: `<ctrl-r>`n`<enter>` <br/>
*Here I use nano on the `ListExamples.java` file. Since the command is in my history, I search for it using `<ctrl-r>`.*

![image5](https://cdn.discordapp.com/attachments/776858501720178758/1079537734714130523/image.png) <br/>
Keys pressed: `<down><right><backspace>`2`<ctrl-o><enter><ctrl-x>` <br/>
*In the nano window, I hold the down arrow key to get to the line of the bug. Once I reached that line, I held down the right arrow key to get the cursor in front of the 1 in `index1`. I then backspace to delete the 1 and type 2 to replace it with 2. Finally I save the file with `<ctrl-o>` and close nano with `<ctrl-x>`*
### Run the tests, demonstrating that they now succeed

![image6](https://cdn.discordapp.com/attachments/776858501720178758/1079538404515139736/image.png) <br/>
Keys pressed:`<up><up><enter><up><up><enter>` <br/>
*Since the compile and running the tester commands were just used in my history, I press up arrow key two times (since it was 2 up in the history) to bring back the command to compile, press enter, then do the same for the command to run the tests.*
### Commit and push the resulting change to your Github account

![image7](https://cdn.discordapp.com/attachments/776858501720178758/1079539010889863228/image.png) <br/>
Keys pressed: `<ctrl-r>`g`<enter>` <br/>
*To simplify committing and pushing, I used the command `git add .;git commit -m "updated";git push origin main`, which executes all the needed commands without me needing to type in and press enter in between each command. Since it was in my history, I searched for it using `<ctrl-r>`.*
