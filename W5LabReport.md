## **Command-Line Options for grep** 
**1. grep -R**
Example 1:
```
% grep -R "Pindling" written_2     
./travel_guides/berlitz2/Bahamas-History.txt:Under a new constitution in 1964, the colony was given self-government with a ministerial-parliamentary system. In 1967 elections, the Progressive Liberal Party was victorious, its leader Lynden O. Pindling becoming premier. Following a constitutional conference in London, the Bahamas became fully independent on July 10, 1973, and is now a member of the United Nations and the British Commonwealth. In August 1992 the Progressive Liberal Party, still headed by Lynden O. Pindling, was toppled by the Free National Movement after 25 years in power. Today’s prime minister is Hubert Ingraham.
``` 
Example 2: 
```
% grep -R "Stanislaw" written_2         
./travel_guides/berlitz2/Poland-History.txt:At the beginning of the 18th century, Poland entered a prolonged period of decline, marked by financial ruin, a debilitated military, and a series of ineffectual kings. Poland was transformed into a client state of the Russians, and then lost much of its western territory to the Prussians during the Silesian Wars that ended in 1763. The following year Stanislaw August Poniatowski was elected the last king of the Polish-Lithuanian Commonwealth, and Poland soon faced one of its most humiliating episodes.
``` 
`grep -R` recusively searches subdirectories which allows it to look for specific strings that may be within multiple layers of directories. This is useful because with it we can search through all subdirectories within a directory at once instead of looking through each subdirectory one by one. I found this command through using the command `man grep`.

  
**2. grep -n**
Example 1:
```
% grep -n "rural" WhereToGreek.txt written_2/travel_guides/berlitz1/WhereToGreek.txt
16:        nightclubs. Here you’ll find much more evidence of the rural life, with
``` 
Example 2:
```
% grep -n "Saturday" written_2/travel_guides/berlitz2/Paris-WhatToDo.txt
8:The majority of shops and department stores are open from 9am to 7pm Tuesday to Saturday. Some shops close for lunch from noon until 2pm and many are closed on Monday mornings, if not all day Monday. The first to open its doors is usually the bakery (boulangerie), and there’s always a small grocer (épicerie) or mini-supermarket in which you can shop until 9 or 10pm, or even midnight. The success of the Marais district’s Sunday opening hours is gradually spreading across town. The drugstore at the top of the Champs-Elysées is open until 2am every night for snacks, take-out food, books, assorted gifts, and essentials.
16:Flea markets (Marchés aux Puces). The experts leave few real bargains among the old treasures, but it’s fun to keep looking. Many of the stands are run by professional dealers. The giant of the flea markets is St-Ouen just north of Porte de Clignancourt métro station, open from 6am to 7pm Saturday, Sunday, and Monday. The market at Porte de Vanves in the 14th arrondissement has a high proportion of junk (open Saturday and Sunday 6am–6pm). You’ll find bric-a-brac and second-hand clothes at Porte de Montreuil, in the 20th, open Saturday, Sunday, and Monday mornings. For inexpensive new clothes, pay a visit to the carreau du Temple, in the 3rd, open every morning except Monday.
20:Food markets. Covered markets or street markets operate all over Paris. On the Left Bank, try the photogenic rue de Buci in St-Germain-des-Prés, open every morning except Monday. Most popular with tourists is rue Mouffetard, behind the Panthéon, on Tuesday, Thursday, and Saturday morning. On the Right Bank, the Wednesday and Saturday market on avenue Président-Wilson has the special elegance of its 16th arrondissement.
```
`grep -n` returns the line number along with the line that the specified string is found within a file. This is useful because instead of searching where the string is within the file, you can use this command to know exactly where it will be. I found this command through using the command `man grep`. 

**3. grep -i**
Example 1: 
```
% grep -i "saturday" written_2/travel_guides/berlitz2/Paris-WhatToDo.txt
The majority of shops and department stores are open from 9am to 7pm Tuesday to Saturday. Some shops close for lunch from noon until 2pm and many are closed on Monday mornings, if not all day Monday. The first to open its doors is usually the bakery (boulangerie), and there’s always a small grocer (épicerie) or mini-supermarket in which you can shop until 9 or 10pm, or even midnight. The success of the Marais district’s Sunday opening hours is gradually spreading across town. The drugstore at the top of the Champs-Elysées is open until 2am every night for snacks, take-out food, books, assorted gifts, and essentials.
Flea markets (Marchés aux Puces). The experts leave few real bargains among the old treasures, but it’s fun to keep looking. Many of the stands are run by professional dealers. The giant of the flea markets is St-Ouen just north of Porte de Clignancourt métro station, open from 6am to 7pm Saturday, Sunday, and Monday. The market at Porte de Vanves in the 14th arrondissement has a high proportion of junk (open Saturday and Sunday 6am–6pm). You’ll find bric-a-brac and second-hand clothes at Porte de Montreuil, in the 20th, open Saturday, Sunday, and Monday mornings. For inexpensive new clothes, pay a visit to the carreau du Temple, in the 3rd, open every morning except Monday.
Food markets. Covered markets or street markets operate all over Paris. On the Left Bank, try the photogenic rue de Buci in St-Germain-des-Prés, open every morning except Monday. Most popular with tourists is rue Mouffetard, behind the Panthéon, on Tuesday, Thursday, and Saturday morning. On the Right Bank, the Wednesday and Saturday market on avenue Président-Wilson has the special elegance of its 16th arrondissement.
```
Example 2:
```
% grep -i "samothraki" written_2/travel_guides/berlitz1/WhereToGreek.txt
        and the northern Aegean islands of Samothraki, Limnos, and Thasos. We
        Samothraki
        A series of rocky cliffs line the shoreline of Samothraki
        of Christianity, Samothraki was a very important island indeed.
        where archaeologists found the Winged Victory of Samothraki, now in the
```
`grep -i` returns the line that contains the specified string regardless of capitilization. This is useful to check for strings that could potentialy have upper and/or lowercases. I found this command through using the command `man grep`.  
**4. grep -c**
```
% grep -c "were" written_2/non-fiction/OUP/Abernathy/ch1.txt    
7
```
```
% grep -c "and" written_2/non-fiction/OUP/Berk/ch1.txt  
143
```
`grep -c` returns the count of the lines that contain the specified string. This is useful to quickly check for the frequency of a word in a file; especially if that word was used a lot.
