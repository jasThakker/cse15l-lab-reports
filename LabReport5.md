# Lab Report 5.

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
```
Example 2
cd written_2/
grep -i "lUcayANs" ./*/*/*
grep: ./non-fiction/OUP/Abernathy: Is a directory
grep: ./non-fiction/OUP/Berk: Is a directory
grep: ./non-fiction/OUP/Castro: Is a directory
grep: ./non-fiction/OUP/Fletcher: Is a directory
grep: ./non-fiction/OUP/Kauffman: Is a directory
grep: ./non-fiction/OUP/Rybczynski: Is a directory
./travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
./travel_guides/berlitz2/Bahamas-History.txt:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```
grep is a powerfull command that can be used to search a particular pattern through text files, and this command can be used with different options like grep -i to widen the scope of its functionality. The grep -i command searches through and returns the file that have the pattern we are searching for irrespective of the case its written in.
In example 1 the command accuaretely counts and returns that 224 lines in findResults.txt have the ".txt" extension even though the pattern to be found is ".TXt".

In example 2 the grep -i command searches through text files in the written_2 and displays where the pattern "lUcayANs" is found and this search is case insensitve



**Command: grep -v "pattern" filename** 
```
Example 1
grep -v ".txt" findResults.txt |wc
     12      12     355
```

```
Example 2
 grep -v "Lucayans" ./*/*/*| wc
grep: ./non-fiction/OUP/Abernathy: Is a directory
grep: ./non-fiction/OUP/Berk: Is a directory
grep: ./non-fiction/OUP/Castro: Is a directory
grep: ./non-fiction/OUP/Fletcher: Is a directory
grep: ./non-fiction/OUP/Kauffman: Is a directory
grep: ./non-fiction/OUP/Rybczynski: Is a directory
  60828 1060999 9272147
```
The option "-v" when used with the grep command searches for the pattern through the file and returns the lines that do NOT contain the pattern.
In example 1 the grep -v command searches for the pattern ".txt" through the file findResults.txt and since wc is used it accurately counts and returns that 12 lines don't contain the ".txt" extentsion

In example 2 the grep -v command searches for the pattern "Lucayans" through all the text files in the written_2 directory and the wc command counts and returns that 60829 lines don't contain that word.



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

```
Example 2
grep -n "Lucayans" ./*/*/*    
grep: ./non-fiction/OUP/Abernathy: Is a directory
grep: ./non-fiction/OUP/Berk: Is a directory
grep: ./non-fiction/OUP/Castro: Is a directory
grep: ./non-fiction/OUP/Fletcher: Is a directory
grep: ./non-fiction/OUP/Kauffman: Is a directory
grep: ./non-fiction/OUP/Rybczynski: Is a directory
./travel_guides/berlitz2/Bahamas-History.txt:6:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
./travel_guides/berlitz2/Bahamas-History.txt:7:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```
The -n option when used with the grep command displays the lines where the pattern appears along with the line numbers. This can be particulary usefull if a pattern has multiple occurences in a long text file, using this command we can easily know the line numbers where the pattern appears in the text files rather than having to count lines manually.
In example 2 we see that using the grep -n option is very useful because it searches through all the files in the written_2 folder for the word "Lucayans" and displays that it is found in the file Bahamas-History.txt on line 6 and on line 7



**Command: grep -c "pattern" filename** 
```
Example 1
docsearch:507$ grep -c ".txt" findResults.txt
224
```

```
Example 2
berlitz2:534$ grep -c "Lucayans" ./*  
./Algarve-History.txt:0
./Algarve-Intro.txt:0
./Algarve-WhatToDo.txt:0
./Algarve-WhereToGo.txt:0
./Amsterdam-History.txt:0
./Amsterdam-Intro.txt:0
./Amsterdam-WhatToDo.txt:0
./Amsterdam-WhereToGo.txt:0
./Athens-History.txt:0
./Athens-Intro.txt:0
./Athens-WhatToDo.txt:0
./Athens-WhereToGo.txt:0
./Bahamas-History.txt:2
./Bahamas-Intro.txt:0
./Bahamas-WhatToDo.txt:0
./Bahamas-WhereToGo.txt:0
./Bali-History.txt:0
.
.
.
NOTE THAT I HAVE NOT INCLUDED THE ENTIRE OUTPUT AS IT WAS VERY LONG
```
The -c option when used with the grep command counts and displays the number of occurences of the pattern in the file we are searching in.
In example 1 it displays 224 because the ".txt" extension appears in 224 lines in the findResults.txt file and so it can be used as a replacement for the wc command.

In example 2 if we particularly find of the word "Lucayans" in the berlitz 2 directory the command displays how all text files other than Bahamas_History.txt have 0 occurences of the word and Bahamas_History.txt has two occurences as we had found before

Source: I got some more clarity and information about different grep command line options using Chat GPT [Link](https://chat.openai.com/)
