# Lab Report 3

**Command chosen: find**

**Four interesting command line options:**

* find . -iname
* find ~/folderName -mtime -1
* find . -name 'sampleName*': 
* find . -type d -empty -delete: 



**Command:find . -iname** 
```
Example 1
jasthakker@Jass-MacBook-Pro written_2 % cd travel_guides
jasthakker@Jass-MacBook-Pro travel_guides % cd berlitz2
jasthakker@Jass-MacBook-Pro berlitz2 % find . -iname "bali-history.txt"
./Bali-History.txt
```
```
Example 2
jasthakker@Jass-MacBook-Pro written_2 % cd non-fiction
jasthakker@Jass-MacBook-Pro non-fiction % cd OUP
jasthakker@Jass-MacBook-Pro OUP % cd Berk
jasthakker@Jass-MacBook-Pro Berk % find . -iname "Ch7.txt"         
./ch7.txt
```
This command finds file names with a specified regex which is case insensitive. In the above examples I tried to find the given files with their filenames with incorrected capitalization of alphabets however since the find iname command is case insensitive it yielded the desired results.


**Command:find ./folderName -mtime -1**
```
Example 1
// Had intentionally made changes in HandRHawaii.txt to test functioning of this command
jasthakker@Jass-MacBook-Pro written_2 % find ./travel_guides -mtime -1
./travel_guides/berlitz1/HandRHawaii.txt
```

```
Example 2
// Had intentionally made changes in another file Algarve-WhatToDo.txt to test functioning of this command
jasthakker@Jass-MacBook-Pro written_2 % find ./travel_guides -mtime -1
./travel_guides/berlitz1/HandRHawaii.txt
./travel_guides/berlitz2/Algarve-WhatToDo.txt
```
Finds files in a particular folder that have been modified in the last 24hrs




**Command:find . -name 'sampleName*'**
```
Example 1
jasthakker@Jass-MacBook-Pro berlitz2 % find . -name 'Barcelona*'
./Barcelona-History.txt
./Barcelona-WhereToGo.txt
./Barcelona-WhatToDo.txt
```

```
Example 2
jasthakker@Jass-MacBook-Pro written_2 % cd travel_guides
jasthakker@Jass-MacBook-Pro travel_guides % cd berlitz1
jasthakker@Jass-MacBook-Pro berlitz1 % find . -iname 'hand*'
./HandRLasVegas.txt
./HandRIstanbul.txt
./HandRJamaica.txt
./HandRHongKong.txt
./HandRLisbon.txt
./HandRMallorca.txt
./HandRLosAngeles.txt
./HandRMadeira.txt
./HandRIbiza.txt
./HandRIsrael.txt
./HandRLakeDistrict.txt
./HandRMadrid.txt
./HandRJerusalem.txt
./HandRHawaii.txt
```
 Finds files that start with a particular specified text regex. In Example 2 I combined and used 2 commands, find . -iname and find . -name 'sampleName*'
 by using lower case hand to find all files that start with upper case Hand.
 
 
 
 **Command :find . -type d -empty -delete
 ```
 Example 1
 jasthakker@Jass-MacBook-Pro written_2 % ls
non-fiction     travel_guides
jasthakker@Jass-MacBook-Pro written_2 % mkdir emptyDir
jasthakker@Jass-MacBook-Pro written_2 % ls
emptyDir        non-fiction     travel_guides
jasthakker@Jass-MacBook-Pro written_2 % find . -type d -empty -delete
jasthakker@Jass-MacBook-Pro written_2 % ls
non-fiction     travel_guides
```

```
Example 2
jasthakker@Jass-MacBook-Pro written_2 % cd travel_guides
jasthakker@Jass-MacBook-Pro travel_guides % ls
berlitz1        berlitz2
jasthakker@Jass-MacBook-Pro travel_guides % mkdir emptyTravelGuides
jasthakker@Jass-MacBook-Pro travel_guides % ls
berlitz1                berlitz2                emptyTravelGuides
jasthakker@Jass-MacBook-Pro travel_guides % find . -type d -empty -delete             
jasthakker@Jass-MacBook-Pro travel_guides % ls
berlitz1        berlitz2
```
This command finds and deletes empty directories. In the two examples above I intentionally created empty directories inside the written_2 directory  and travel_guides directory and ran this command and it can be seen that the empty directories got deleted.

All options were referred from this [website](https://ss64.com/bash/find.html)
