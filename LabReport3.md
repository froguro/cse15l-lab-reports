# **Lab Report 3**

## `find`
I will be focusing on the `find` command

### **Option 1: `-empty`**
Searches for empty files and directories.

**Example 1** <br>
```
[cs15lwi23axq@ieng6-202]:skill-demo1-data:262$ ls written_2
empty_file.txt  non-fiction  travel_guides
[cs15lwi23axq@ieng6-202]:skill-demo1-data:263$ find written_2 -empty
written_2/empty_file.txt
```
After creating an empty text file in written_2, using `find written_2 -empty` will search through written_2 to return all empty files and directories. Because there is an empty file, it returns `written_2/empty_file.txt`. This is useful for any case where you need to find an empty file in a large directory.

**Example 2** <br>
```
[cs15lwi23axq@ieng6-202]:skill-demo1-data:265$ find written_2/non-fiction -empty
[cs15lwi23axq@ieng6-202]:skill-demo1-data:266$ 
```
Trying to find an empty file in the non-fiction directory, it can be seen that nothing is returned because there is no empty file or directory within non-fiction. This is useful to show that there are not any empty files or directories laying around.


### **Option 2: `-newer file`**
Searches for files that were modified/created after ‘file’.

**Example 1** <br>
```
[cs15lwi23axq@ieng6-202]:skill-demo1-data:268$ find written_2 -newer written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
written_2
written_2/travel_guides/berlitz2
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
written_2/empty_file.txt
```
Using `-newer` on this file called Vallarta-WhatToDo.txt, it returns directories and files that were modified or created after it. This is useful to find which files were created or changed after a certain point.

**Example 2** <br>
```
[cs15lwi23axq@ieng6-202]:skill-demo1-data:269$ find written_2 -newer written_2/empty_file.txt                              
[cs15lwi23axq@ieng6-202]:skill-demo1-data:270$ 
```
Using `-newer` on the newest file in written_2 will return nothing because there were no changes or creations made after it yet. This is useful to see that a file is the newest file.

### **Option 3: `-exec CMD`**
Executes CMD on directories and files being searched

**Example 1** <br>
```
[cs15lwi23axq@ieng6-202]:skill-demo1-data:285$ find written_2 -exec grep "Hello" {} \;
grep: written_2: Is a directory
grep: written_2/non-fiction: Is a directory
grep: written_2/non-fiction/OUP: Is a directory
grep: written_2/non-fiction/OUP/Abernathy: Is a directory
grep: written_2/non-fiction/OUP/Berk: Is a directory
Children’s earliest efforts at make-believe also reveal how challenging they ﬁnd the task of detaching thought from reality. Initially, object substitutions are closely tied to the real things they represent. Toddlers between ages 1 1/2 and 2 generally use only realistic-looking objects while pretending—a toy telephone to talk into or a cup to drink from.9 Once, I handed a 21-month-old a small wooden block, put another to my ear, and called her on the phone: “Ring! Ring! Hello, Lynnay!” She responded by throwing down the block and turning to another activity. Yet when given a plastic replica of a push-button phone, Lynnay readily put the receiver to her ear and pretended to converse.
As children engage in play talk, they not only build their vocabularies but correct one another’s errors, either directly or by demonstrating the acceptable way to speak. In one instance, a kindergartner enacting a telephone conversation said, “Hello, come to my house, please.” Her play partner quickly countered with appropriate telephone greeting behavior: “No, ﬁrst you’ve got to say ‘How are you? What are you doing?’”28
grep: written_2/non-fiction/OUP/Castro: Is a directory
grep: written_2/non-fiction/OUP/Fletcher: Is a directory
grep: written_2/non-fiction/OUP/Kauffman: Is a directory
grep: written_2/non-fiction/OUP/Rybczynski: Is a directory
grep: written_2/travel_guides: Is a directory
grep: written_2/travel_guides/berlitz1: Is a directory
        Saint-Wandrille, Le Bec-Hellouin, and Caen, culminating in their
grep: written_2/travel_guides/berlitz2: Is a directory
```
This command searches through written_2 and then prints out any file that contains the string Hello. It can be seen when directories are searched since grep cannot be used on directories. This command is useful to quickly find what file in a directory contains a certain string.

**Example 2** <br>
```
[cs15lwi23axq@ieng6-202]:skill-demo1-data:286$ find written_2 -name WhatToLosAngeles.txt -exec wc {} \;
  369  3383 24076 written_2/travel_guides/berlitz1/WhatToLosAngeles.txt
```
This command finds the file named WhatToLosAngeles.txt and then executes the wc command on it. It returns the wc of the text file. This is useful because prior to this we would probably first take the result of find into a new file and use wc on that new file. This speeds up the process significantly.

### **Option 4: `-ok CMD`**
Works like `-exec` but it prompts the user first.

**Example 1:** <br>
```
[cs15lwi23axq@ieng6-202]:skill-demo1-data:312$ find written_2/non-fiction/OUP/Rybczynski -name "*.txt" -ok wc {} \;
< wc ... written_2/non-fiction/OUP/Rybczynski/ch1.txt > ? y
   60  5356 34412 written_2/non-fiction/OUP/Rybczynski/ch1.txt
< wc ... written_2/non-fiction/OUP/Rybczynski/ch2.txt > ? n
< wc ... written_2/non-fiction/OUP/Rybczynski/ch3.txt > ? y
   70  8062 52179 written_2/non-fiction/OUP/Rybczynski/ch3.txt
```
This command goes through the .txt files in the given directory and gives the wc of each, only if you say yes after it prompts you. This is useful if you only wanted to find the wc of certain files.

**Example 2:** <br>
```
[cs15lwi23axq@ieng6-202]:skill-demo1-data:348$ find written_2/non-fiction/OUP/Rybczynski -name "*.txt" -ok cat {} \;
< cat ... written_2/non-fiction/OUP/Rybczynski/ch1.txt > ? n
< cat ... written_2/non-fiction/OUP/Rybczynski/ch2.txt > ? n
< cat ... written_2/non-fiction/OUP/Rybczynski/ch3.txt > ? n
```
This command goes through the .txt files in the given directory and prompts to print out the contents of each file. This is useful if you want to print out some results from the find command.
