# The Archivist

First of all, all flags have the same structure: ZDTM{...}

# Challenge 1 

The archivist claimed his encryption was impossible to reverse.

392b322b1e3d2c3d392a2a2a283c39352624312623343a312b2e28392c313c26351b

First of all after trying a lot of different combinations of decryption using CyberChef I decided to try using the XOR Cipher on the string.

I used the key "ZDTM" because it was the only string I knew for sure would exist in the string.

<img width="784" height="433" alt="image" src="https://github.com/user-attachments/assets/e3ed3cdc-286d-4a34-b0d1-a57dbb55c4fe" />

After that i noticed that the begging of the new string looks too similar to the word "coffee" to be a coincidence so i decided to use it as the new key.

<img width="780" height="425" alt="image" src="https://github.com/user-attachments/assets/08537caa-65a0-4c93-9627-62e3d03054d8" />

Website used: https://www.dcode.fr/xor-cipher

# Challenge 2

The archivist thought he learned from his previous mistake. Did hex?

576b525554587446546b4e5052456c4f5231394a5531394f5431526652553544556c6c5156456c50546e303d

Using the author's suggestion I decrypted the string using hex.

<img width="1282" height="548" alt="image" src="https://github.com/user-attachments/assets/a211d385-4f07-4dd6-8acd-405e7d234d16" />

After that I noticed that the new string looks very familiar to base64 so I used that on it and there was the flag!

<img width="1264" height="588" alt="image" src="https://github.com/user-attachments/assets/6dedd1f0-f0c9-4f56-938f-02d0d7b60559" />

Webiste used: https://gchq.github.io/CyberChef/

# Challenge 3

A handwritten poem was found beside this one.
~
A fost o datÄ ca-n poveČti,
A fost ca niciodatÄ,
Din rude mari ĂŽmpÄrÄteČti,
O prea frumoasÄ fatÄ.

Či era una la pÄrinČi
Či mĂ˘ndrÄ-n toate cele,
Cum e Fecioara ĂŽntre sfinČi
Či luna ĂŽntre stele.

Din umbra falnicelor bolČi
Ea pasul Či-l ĂŽndreaptÄ
LĂ˘ngÄ fereastrÄ, unde-n colČ
LuceafÄrul aČteaptÄ.

Privea ĂŽn zare cum pe mÄri
RÄsare Či strÄluce,
Pe miČcÄtoarele cÄrÄri
CorÄbii negre duce.
~

KXVQ{RJTVNL_AYPXRZ_CZICMU_CVDJLVHPLMEE}

Here is a famous romanian poem called "Luceafarul" written by Mihai Eminescu.
At first the string bellow looked like Caesar Cypher but I was mistaken.
After that I used Vignere Cypher on the string with the key "Luceafarul", the name of the poem.

<img width="767" height="447" alt="image" src="https://github.com/user-attachments/assets/6b069555-069e-445f-86e9-32fe0cb3c79c" />

Webisite used: https://www.dcode.fr/vigenere-cipher

# Challenge 4

The archivist finally embraced modern cryptography.
âClassical ciphers are toys, small ones.â he wrote.

n = 9408759790383105133161103283826984827528801769314347714547601915589546181131310708353405753091496859205091371436900900073486088639260461160646631812396469191626982296459097662217285121344426946437706688765214301460605941543495147614538135179544829052420146985668806196559606619586945914030818145149242966368601218719771454948665607889306922955823737265010862549
c = 567886008628582614176675620746647119465913033360839517687380864877007072129989292654535142001555437419581434044085652122402650313910654692956127217631833360125025628559064580874755354513570531922546942280774567523237772780062859047730901058285040490649449603255699250100384409113828519700779759650108805781802193138736539749

Obvious RSA encryption, we were given the encrypted message ( c ) and the public key ( n ). I replaced the encrypted message field and the public key field with the given values and left everything else on default.

<img width="766" height="543" alt="image" src="https://github.com/user-attachments/assets/24b905ce-4f31-4285-a1d4-950b8f3ca3be" />

Website used: https://www.dcode.fr/rsa-cipher

# Challenge 5.

"I am too old for this.
I'll give you the flag, just help me encrypt this message using the 4 column thingy.
Forgot it's name. Btw, X"

JUSTMOVELETTERSNOTTHEMEANINGNOW

First of all I had to search the name of the algorithm the author was reffering: "the 4 column thingy"
After some research I learned that the name of the cipher is Transposition Cipher and it only has 4 columns when the key is exactly 4 characters long.
The string we need to encrypt has a clear meaning, we have to just move the letters so the key will be 4 characters in ascending value ASCII wise ( A B C D or 1 2 3 4 )
We also get the hind that we should add "X" at the end of the message ( "Btw,X")

<img width="429" height="265" alt="image" src="https://github.com/user-attachments/assets/653a7493-a2a7-4f04-b381-c8987fcff95b" />
<img width="334" height="77" alt="image" src="https://github.com/user-attachments/assets/e0f2101e-654a-4832-b174-8efdf4eb46bf" />


The flag is: `ZDTM{JMLEOENNUOERTMIOSVTSTENWTETNHAGX}`

Website used: https://www.dcode.fr/transposition-cipher


# Comoara Nationala

In this challenge we get a zip file with a flag.txt file locked behind a password and a cryptic .txt file.

B:14:50:8
B:3:17:2
PLHA:1:20:3
MCN:8:115:7
LTI:1:1:5
MCN:15:36:1
B:6:42:4
PLHA:1:109:1
MCN:1:6:5
LTI:1:3:2
PLHA:1:67:1 
LTI:1:3:1
LTI:1:2:3
LTI:1:2:1
MCN:3:4:3
B:10:77:6
LTI:1:1:3
B:11:70:4
PLHA:1:73:5
MCN:13:92:2
PLHA:1:345:5 
B:1:6:7
PLHA:1:211:3
B:12:24:3

The description makes it clear that this cryptic text is related to some well known romanian classics.
Every row is a combination of # NAME:CHAPTER:WORD:CHARACTER.
Each name is an abreviation of a romanian classic:
B - Baltagul by Mihail Sadoveanu https://scoala-gropnita.ro/wp-content/uploads/2025/02/Baltagul-de-Mihail-Sadoveanu.pdf
PLHA - Povestea lui Haraap Alb by Ion Creanga https://oradeliteratura.wordpress.com/wp-content/uploads/2009/06/ion-creanga-povestea-lui-harap-alb.pdf
MCN - Moara cu noroc by Ioan Slavici https://www.scoalaluceafarul.ro/carti/moara_cu_noroc.pdf
LTI - Leoaica tanara,iubirea by Nichita Stanescu  https://www.romanianvoice.com/poezii/poezii/leoaica.php

Let's do the first one as an example!
B:14:50:8 means the first character is in the book Baltagul in chapter 14 in the 50'th word at the 8'th position.
Keep in mind that in romanian grammar something structures using " - " count as two words (si-a , v-a , intr-o etc.)
The first step is to go to the virtual version of the book (the links for all of them are above)
Second we need to search for the chapter 14 (CTRL + F Capitolul 14)
<img width="617" height="775" alt="image" src="https://github.com/user-attachments/assets/67d8eeb9-8b0f-4895-98d1-36fb871b77fa" />
Third we need to copy a chunk of text and paste it in a word file (it counts the words for us).
<img width="840" height="757" alt="image" src="https://github.com/user-attachments/assets/44b47ed0-b3bb-475c-b907-e39d1a051a88" />
Forth we need to trim it to the word we need (in our case the 50th) and search how many " - " we have.
<img width="1135" height="860" alt="image" src="https://github.com/user-attachments/assets/aa888385-0414-458b-94da-fa5cbb22601b" />
Fifth we need to backtrack from the final word the number of " - " we found ( to get to the real 50th word)
<img width="1042" height="275" alt="image" src="https://github.com/user-attachments/assets/270cdeae-0581-4a40-abab-066cf7c56f78" />
Sixth we need to get right character (in our case 8)
<img width="1465" height="553" alt="image" src="https://github.com/user-attachments/assets/8c6d512e-04ea-489f-950a-9373144c633c" />

The first letter of our string is : E
After completing the whole thing the string is : euamivitcuvintepotrivite

Using this string as the password for the flag.txt file reveals to us the Flag




















