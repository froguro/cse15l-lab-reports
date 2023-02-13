# **Lab Report 3**

## `find`
I will be focusing on the `find` command

**Command 1: `-empty`**
Searches for empty files and directories.

**Example 1** <br>
```
[cs15lwi23axq@ieng6-202]:skill-demo1-data:262$ ls written_2
empty_file.txt  non-fiction  travel_guides
[cs15lwi23axq@ieng6-202]:skill-demo1-data:263$ find written_2 -empty
written_2/empty_file.txt
```
Using `find written_2 -empty` will search from the directory written_2 any empty file/directory.
Since there are no empty files or directories within written_2, the command will return nothing.
![noempty](Lab3SC2.png)

If I were to create an empty text file in the written_2 directory, then `find written_2 - empty` will return that file.
