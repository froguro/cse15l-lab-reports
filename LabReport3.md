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


