# Lab Report 5

**Command chosen: grep**

**Four interesting command line options:**

* grep -i "pattern" filename
* grep -v "pattern" filename
* grep -n "pattern" filename
* grep -c "pattern" filename



**Command: grep -i "pattern" filename** 
```
Example 1
find written_2 > findResults.txt
[cs15lwi23awm@ieng6-202]:docsearch:505$  grep -i ".TXt" findResults.txt |wc
    224     224   11268
```

grep is a powerfull command that can be used to search a particular pattern through text files, and this command can be used with different options like grep -i to widen the scope of its functionality. The grep -i command searches through and returns the file that have the pattern we are searching for irrespective of the case its written in.
In example 1 the command accuaretely counts and returns that 224 lines in findResults.txt have the ".txt" extension even though the pattern to be found is ".TXt".



**Command: grep -v "pattern" filename** 
```
Example 1
grep -v ".txt" findResults.txt |wc
     12      12     355
```
The option "-v" when used with the grep command searches for the pattern through the file and returns the lines that do NOT contain the pattern.
In example 1 the grep -v command searches for the pattern ".txt" through the file findResults.txt and since wc is used it accurately counts and returns that 12 lines don't contain the ".txt" extentsion



**Command: grep -n "pattern" filename** 
```
Example 1
docsearch:506$ grep -n ".txt" findResults.txt
5:written_2/non-fiction/OUP/Abernathy/ch1.txt
6:written_2/non-fiction/OUP/Abernathy/ch14.txt
7:written_2/non-fiction/OUP/Abernathy/ch15.txt
8:written_2/non-fiction/OUP/Abernathy/ch2.txt
9:written_2/non-fiction/OUP/Abernathy/ch3.txt
10:written_2/non-fiction/OUP/Abernathy/ch6.txt
11:written_2/non-fiction/OUP/Abernathy/ch7.txt
12:written_2/non-fiction/OUP/Abernathy/ch8.txt
13:written_2/non-fiction/OUP/Abernathy/ch9.txt
15:written_2/non-fiction/OUP/Berk/CH4.txt
16:written_2/non-fiction/OUP/Berk/ch1.txt
17:written_2/non-fiction/OUP/Berk/ch2.txt
18:written_2/non-fiction/OUP/Berk/ch7.txt
20:written_2/non-fiction/OUP/Castro/chA.txt
21:written_2/non-fiction/OUP/Castro/chB.txt
22:written_2/non-fiction/OUP/Castro/chC.txt
23:written_2/non-fiction/OUP/Castro/chL.txt
24:written_2/non-fiction/OUP/Castro/chM.txt
25:written_2/non-fiction/OUP/Castro/chN.txt
26:written_2/non-fiction/OUP/Castro/chO.txt
27:written_2/non-fiction/OUP/Castro/chP.txt
28:written_2/non-fiction/OUP/Castro/chQ.txt
29:written_2/non-fiction/OUP/Castro/chR.txt
30:written_2/non-fiction/OUP/Castro/chV.txt
31:written_2/non-fiction/OUP/Castro/chW.txt
32:written_2/non-fiction/OUP/Castro/chY.txt
33:written_2/non-fiction/OUP/Castro/chZ.txt
35:written_2/non-fiction/OUP/Fletcher/ch1.txt
36:written_2/non-fiction/OUP/Fletcher/ch10.txt
37:written_2/non-fiction/OUP/Fletcher/ch2.txt
.
.
.
NOTE THAT I HAVE NOT INCLUDED THE ENTIRE OUTPUT AS IT WAS VERY LONG
```
The -n option when used with the grep command displays the lines where the pattern appears along with the line numbers. This can be particulary usefull if a pattern has multiple occurences in a long text file, using this command we can easily know the line numbers where the pattern appears in the text files rather than having to count lines manually.



**Command: grep -c "pattern" filename** 
```
Example 1
docsearch:507$ grep -c ".txt" findResults.txt
224
```
