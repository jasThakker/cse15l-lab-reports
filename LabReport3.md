# Lab Report 3

**Command chosen: find**

**Four interesting command line options:**

* find . -iname
* find ~/folderName -mtime -1 : Finds files in a particular folder that have been modified in the last 24hrs
* find . -name name 'sampleName*': Finds files that start with a particular specified text regex
* find . -type d -empty -delete: Finds and deletes empty directories



* **Command:find . -iname** 
```
Example 1
jasthakker@Jass-MacBook-Pro written_2 % cd travel_guides
jasthakker@Jass-MacBook-Pro travel_guides % cd berlitz2
jasthakker@Jass-MacBook-Pro berlitz2 % find . -iname "bali-history.txt"
./Bali-History.txt
```
```
jasthakker@Jass-MacBook-Pro written_2 % cd non-fiction
jasthakker@Jass-MacBook-Pro non-fiction % cd OUP
jasthakker@Jass-MacBook-Pro OUP % cd Berk
jasthakker@Jass-MacBook-Pro Berk % find . -iname "Ch7.txt"         
./ch7.txt
```
This command finds file names with a specified regex which is case insensitive. In the above examples I tried to find the given files with their filenames with incorrected capitalization of alphabets however since the find iname command is case insensitive it yielded the desired results.


