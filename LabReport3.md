# **Lab Report 3**

## `find`
I will be focusing on the `find` command

### **Command 1: `-empty`**
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


### **Command 2: `-newer file`**
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
