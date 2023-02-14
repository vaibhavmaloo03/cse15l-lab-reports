# Week 5 Lab report
Using 4 different types of grep commands
## Sources:
[GeeksforGeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

[ChatGPT](https://chat.openai.com/chat)
## grep -c
This command prints the number of lines that match a pattern

```
$ grep -c 1 PuertoRico-History.txt
15
```

The command "grep -c 1 PuertoRico-History.txt" searches for the number of lines in the file "PuertoRico-History.txt" that contain the pattern "1". The "-c" option instructs grep to display only the count of matching lines, rather than the actual lines themselves.

```
$ grep -c "In recent elections, power has alternated between parties" PuertoRico-History.txt
1
```

same way, this searches for "In recent elections, power has alternated between parties" and displays the count of matching lines

## grep -rl
The commant recursively searches for all the files that conatains the pattern and returns the name of the matching file.

```
$ grep -l "In recent elections,"
PuertoRico-History.txt
```

The command "grep -l 'In recent elections,' " recursively searches for all files in the current directory that contain the exact phrase "In recent elections," and prints the names of the matching files to the terminal.


```
$ grep -rl "population"
chA.txt
chB.txt
chC.txt
chL.txt
chQ.txt
chR.txt
chV.txt
```

the same way, this searches for the exact phrase "In recent "population" and prints the names of the matching files to the terminal.

## grep -o

This command prints the exact line of that contains the pattern.

```
$ grep -o "population" chA.txt
population
population
```
The command grep -o "population" chA.txt searches for the exact word "population" in the file "chA.txt" and prints each occurrence of it on a separate line.

```
grep -o "no word" chA.txt
```

this prints nothing since "no word" isn't found in chA.txt

## grep -A n

This command prints searched line and and n lines after

```
grep -A 3 "For Chicanos born in the United States" chA.txt
Aztlán is the Chicano homeland, especially for those coming of age during the 1960s and 1970s, who wanted to create a cultural space that they could call their own. For Chicanos born in the United States, Mexico is not home, but neither is the United States, so Aztlán is looked upon as the mythical homeland. The affiliation with Aztlán also reaffirms the Chicanos’ identity as mestizos (people of mixed ancestry), as members of the indigenous population of the New World. Chicano writers explore the various meanings of Aztlán in an anthology edited by Rudolfo Anaya and Francisco Lomelí titled Aztlán: Essays on the Chicano Homeland.
References Anaya and Lomelí 1989; Barrera 1988; Bierhorst 1990; Chavez 1984; Leal 1995; Valdez and Steiner 1972
```

prints 3 lines after the line that contains "For Chicanos born in the United States".

```
grep -A 1 "(1881-1965)"
Otero-Warren, Nina (Adelina) (1881–1965)
Nina Otero-Warren is known primarily as the writer of the book Old Spain in Our Southwest (1936), a memoir of life in early New Mexico. It is more than an autobiography, since it is interspersed with folklore narratives, Hispano traditions, and early southwest history. Nina Otero was born in Los Lunas, New Mexico, a town named after her grandfather’s family, a descendent of an early influential Hispanic family. They were fairly wealthy and the marriage of her mother and father in 1880 was lavish and elaborate. The details of the wedding are well described by Charlotte Whaley in her biography of Nina. Her father, a member of the famous Otero family, was killed in a shoot-out when Nina was still a baby, and her mother later married A. M. Bergere. They had a large family together, all of whom are well-known citizens of New Mexico. Nina attended school on the East Coast, married and divorced, and eventually settled into New Mexican politics. She was appointed superintendent of schools in the Santa Fe area and was active in the Congressional Union and the Republican Party and lobbied for the vote for women in 1920. In 1922 she ran for the U.S. House of Representatives but was defeated. She continued working for government agencies as an educator and supporter of Indian education. In the early 1960s she worked as a consultant for the Peace Corps, which had a training program at the University of New Mexico in Albuquerque. Like her contemporaries Cleofas Jaramillo and Aurora Lucero-White, she had an interest in folklore, and her book Old Spain in Our Southwest was one of the first private ethnographies to be published by a woman of her era. In it she describes the early Spanish settlers, life on the hacienda, the religious fiestas, the santos (saints), foods, folk songs, folktales, and the customs of the region. In her later years, up until her death in 1965, she was a businesswoman in Santa Fe.
```

prints 1 lines after the line that contains "(1881-1965)"
> This looks more that one single line but its only one. 





