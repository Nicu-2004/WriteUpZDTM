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

<img width="774" height="446" alt="image" src="https://github.com/user-attachments/assets/cbbacad1-82e1-446b-baeb-2ff03360b7fa" />

The flag is: `ZDTM{JLONUETISTTNTTHGMEENORMOVSEWENA}`



