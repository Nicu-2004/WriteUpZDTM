# The Archivist

First of all, all flags have the same structure: ZDTM{...}

# Challenge 1 
```
The archivist claimed his encryption was impossible to reverse.

392b322b1e3d2c3d392a2a2a283c39352624312623343a312b2e28392c313c26351b
```

First of all after trying a lot of different combinations of decryption using CyberChef I decided to try using the XOR Cipher on the string.

I used the key "ZDTM" because it was the only string I knew for sure would exist in the string.

<img width="784" height="433" alt="image" src="https://github.com/user-attachments/assets/e3ed3cdc-286d-4a34-b0d1-a57dbb55c4fe" />

After that i noticed that the begging of the new string looks too similar to the word "coffee" to be a coincidence so i decided to use it as the new key.

<img width="780" height="425" alt="image" src="https://github.com/user-attachments/assets/08537caa-65a0-4c93-9627-62e3d03054d8" />

Website used: https://www.dcode.fr/xor-cipher

# Challenge 2
```
The archivist thought he learned from his previous mistake. Did hex?

576b525554587446546b4e5052456c4f5231394a5531394f5431526652553544556c6c5156456c50546e303d
```
Using the author's suggestion I decrypted the string using hex.

<img width="1282" height="548" alt="image" src="https://github.com/user-attachments/assets/a211d385-4f07-4dd6-8acd-405e7d234d16" />

After that I noticed that the new string looks very familiar to base64 so I used that on it and there was the flag!

<img width="1264" height="588" alt="image" src="https://github.com/user-attachments/assets/6dedd1f0-f0c9-4f56-938f-02d0d7b60559" />

Webiste used: https://gchq.github.io/CyberChef/

# Challenge 3
```
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
```

Here is a famous romanian poem called "Luceafarul" written by Mihai Eminescu.
At first the string bellow looked like Caesar Cypher but I was mistaken.
After that I used Vignere Cypher on the string with the key "Luceafarul", the name of the poem.

<img width="767" height="447" alt="image" src="https://github.com/user-attachments/assets/6b069555-069e-445f-86e9-32fe0cb3c79c" />

Webisite used: https://www.dcode.fr/vigenere-cipher

# Challenge 4
```
The archivist finally embraced modern cryptography.
âClassical ciphers are toys, small ones.â he wrote.

n = 9408759790383105133161103283826984827528801769314347714547601915589546181131310708353405753091496859205091371436900900073486088639260461160646631812396469191626982296459097662217285121344426946437706688765214301460605941543495147614538135179544829052420146985668806196559606619586945914030818145149242966368601218719771454948665607889306922955823737265010862549
c = 567886008628582614176675620746647119465913033360839517687380864877007072129989292654535142001555437419581434044085652122402650313910654692956127217631833360125025628559064580874755354513570531922546942280774567523237772780062859047730901058285040490649449603255699250100384409113828519700779759650108805781802193138736539749
```

Obvious RSA encryption, we were given the encrypted message ( c ) and the public key ( n ). I replaced the encrypted message field and the public key field with the given values and left everything else on default.

<img width="766" height="543" alt="image" src="https://github.com/user-attachments/assets/24b905ce-4f31-4285-a1d4-950b8f3ca3be" />

Website used: https://www.dcode.fr/rsa-cipher

# Challenge 5.

```
I am too old for this.
I'll give you the flag, just help me encrypt this message using the 4 column thingy.
Forgot it's name. Btw, X

JUSTMOVELETTERSNOTTHEMEANINGNOW
```

First of all I had to search the name of the algorithm the author was reffering: "the 4 column thingy"
After some research I learned that the name of the cipher is Transposition Cipher and it only has 4 columns when the key is exactly 4 characters long.
The string we need to encrypt has a clear meaning, we have to just move the letters so the key will be 4 characters in ascending value ASCII wise ( A B C D or 1 2 3 4 )
We also get the hint that we should add "X" at the end of the message ( "Btw,X")

<img width="429" height="265" alt="image" src="https://github.com/user-attachments/assets/653a7493-a2a7-4f04-b381-c8987fcff95b" />
<img width="334" height="77" alt="image" src="https://github.com/user-attachments/assets/e0f2101e-654a-4832-b174-8efdf4eb46bf" />


The flag is: `ZDTM{JMLEOENNUOERTMIOSVTSTENWTETNHAGX}`

Website used: https://www.dcode.fr/transposition-cipher


# Comoara Nationala

In this challenge we get a zip file with a flag.txt file locked behind a password and a cryptic .txt file.
```
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
```
The description makes it clear that this cryptic text is related to some well known romanian classics.
Every row is a combination of  NAME:CHAPTER:WORD:CHARACTER.
Each name is an abreviation of a romanian classic:

`B - Baltagul by Mihail Sadoveanu` [Baltagul-de-Mihail-Sadoveanu.pdf](https://scoala-gropnita.ro/wp-content/uploads/2025/02/Baltagul-de-Mihail-Sadoveanu.pdf)

`PLHA - Povestea lui Haraap Alb by Ion Creanga` [ion-creanga-povestea-lui-harap-alb.pdf](https://oradeliteratura.wordpress.com/wp-content/uploads/2009/06/ion-creanga-povestea-lui-harap-alb.pdf)

`MCN - Moara cu noroc by Ioan Slavici` [moara_cu_noroc.pdf](https://www.scoalaluceafarul.ro/carti/moara_cu_noroc.pdf)

`LTI - Leoaica tanara,iubirea by Nichita Stanescu`  [leoaica.php](https://www.romanianvoice.com/poezii/poezii/leoaica.php)



Let's do the first one as an example!
B:14:50:8 means the first character is in the book Baltagul in chapter 14 in the 50'th word at the 8'th position.
Keep in mind that in romanian grammar, structures using " - " count as two words (si-a , v-a , intr-o etc.).
The first step is to go to the virtual version of the book (the links for all of them are above).
Second we need to search for the chapter 14 (CTRL + F Capitolul 14)
<img width="617" height="775" alt="image" src="https://github.com/user-attachments/assets/67d8eeb9-8b0f-4895-98d1-36fb871b77fa" />

Third we need to copy a chunk of text and paste it in a word file (it counts the words for us).
<img width="840" height="757" alt="image" src="https://github.com/user-attachments/assets/44b47ed0-b3bb-475c-b907-e39d1a051a88" />

Fourth we need to trim it to the word we need (in our case the 50th) and search how many " - " we have.
<img width="1135" height="860" alt="image" src="https://github.com/user-attachments/assets/aa888385-0414-458b-94da-fa5cbb22601b" />

Fifth we need to backtrack from the final word the number of " - " we found ( to get to the real 50th word).
<img width="1042" height="275" alt="image" src="https://github.com/user-attachments/assets/270cdeae-0581-4a40-abab-066cf7c56f78" />
Sixth we need to get right character (in our case 8).
<img width="1465" height="553" alt="image" src="https://github.com/user-attachments/assets/8c6d512e-04ea-489f-950a-9373144c633c" />

The first letter of our string is : 'e'

After completing the whole thing the string is : `euamivitcuvintepotrivite`

Using this string as the password for the flag.txt file reveals to us the flag: `ZDTM{bravo_tinere_sunt_mandru_de_tine}`

# Radial, the Great Knight

' legend has it that he provides a hidden message '

<img width="1200" height="1200" alt="image" src="https://github.com/user-attachments/assets/52444505-5c59-4669-99bf-08f7494810f8" />

At first I had no ideea what the picture meant so I did a reverse image search.
Turns out the image is a well known puzzle in chess called "Knight's Tour". 
The main ideea of the game is that the knight must go on all the squares exactly once starting from a given square (in our case bottom left).
We can see that in the author's picture there are letters and underscores scattered around all the board. We can safely assume that this is how we are going to get our flag.
After trying some variants of the game that worked but didn't get us the right flag we choose to use the algorithm in the Wikipedia article and manually do it ourselves.

<img width="960" height="960" alt="image" src="https://github.com/user-attachments/assets/9a2fca5a-c6ab-42e3-9b1a-8cb362c9d329" />

This is our board looks after I overlapped the algorithm with the board.

<img width="1200" height="1200" alt="image" src="https://github.com/user-attachments/assets/e3e27023-2396-48f1-a00f-a3d0592a6e51" />

Following the lines (starting where our knight is) we get the characters: `THE_REAL_KNIGHTS_MOVE_SEQUENCE_GETS_SHARPER_WITH_MORE_ATTENTION`

The flag is: `ZDTM{THE_REAL_KNIGHTS_MOVE_SEQUENCE_GETS_SHARPER_WITH_MORE_ATTENTION}`


# consent-kiosk
```
Please read and accept our terms.
Btw, HR designed the button to be very respectful of personal space.
```

When I opened the website, the first thing I noticed was the "I agree" button avoiding the mouse.
<img width="773" height="494" alt="image" src="https://github.com/user-attachments/assets/ab67f5f1-7c67-4b2a-920d-3c71cd9cc3fd" />

I opened the console right after, and the website detected it. It didin't take me long to notice that the detection could be bypassed by refreshing the page with the console already open.
<img width="1918" height="918" alt="image" src="https://github.com/user-attachments/assets/719c0bbe-3102-4a93-945c-d421445ace29" />

When I checked the network requests, I noticed a file called `telemetry.js`.
<img width="837" height="513" alt="image" src="https://github.com/user-attachments/assets/d29596da-98c8-4357-87bb-0684397178d6" />

I copied its content to the console, and called the function directly.
<img width="1919" height="910" alt="image" src="https://github.com/user-attachments/assets/7dc81eb8-c62f-4b8e-88f3-fadf623aa5ad" />

# legacy-profile
```
A small portal that lets users update their info, what could go wrong?
```

After I registered to the website, I noticed that a session token was created that had no valid signature.
<img width="659" height="196" alt="image" src="https://github.com/user-attachments/assets/3d2d6086-a1de-4f6e-b272-f2f971e959ed" />

I visited a JWT debugging website ([jwt.io](https://jwt.io)) and changed my roles to become an admin.
<img width="1223" height="855" alt="image" src="https://github.com/user-attachments/assets/90c9aed7-058b-4837-b482-dcd5e9b619bf" />

I removed the signature part of my alterned one and replaced it with `legacy-signature`. Then I visited the admin page.
<img width="1020" height="358" alt="image" src="https://github.com/user-attachments/assets/5997e4bc-d4d7-4499-a18f-a84d0de8ec3b" />

# Open Gallery
```
the gallery accepts anything the artist brings.

Get the flag from /flag.txt
```
I instantly noticed that the website allowed files with any extension to be uploaded. Noticing the PHP headers, I uploaded a small PHP file that could ls and cat each file

<img width="589" height="306" alt="image" src="https://github.com/user-attachments/assets/90c99b36-c18b-47ee-bca7-db28528e25b0" />

After visiting my submission, I was able to get the flag from the root directory.
<img width="968" height="925" alt="image" src="https://github.com/user-attachments/assets/524de7db-e12d-4d3e-9e16-fae7689a542a" />

# MacroPlex
```
Welcome Trainee to the phishing training course!
You have been provided with your task
Q1. What is the email of the recipient?
Q2. What is the extension of the attachment? (for example: pdf, mp3)
Q3. What did you find in the attachment?
```
After opening the .eml file in Outlook, I instantly knew the first 2 questions required to solve the challange.
<img width="1416" height="256" alt="image" src="https://github.com/user-attachments/assets/ff2d45f5-02c3-4ade-b14c-51b9187ecd7f" />

Opening the .docm file in Libreoffice, I got informed that the file contained macros.
<img width="1431" height="741" alt="image" src="https://github.com/user-attachments/assets/044258cc-05e0-4706-a240-6c1363cb42e8" />

Viewing the macro gave me the answer to the third question
<img width="1422" height="741" alt="image" src="https://github.com/user-attachments/assets/3af15604-f294-4212-926c-a45ec2d75094" />

The flag was: `ZDTM{Mara.M@macroplex.com_docm_m4lw4re}`

# in-plain-sight
```
dw about it DW is full of mysteries [=
```
I opened the pcap file in Wireshark, and noticed a peculiar response to a request containing a jpeg image
<img width="1919" height="1037" alt="image" src="https://github.com/user-attachments/assets/88d87851-a370-47a7-83b4-31632dc7ef97" />

I copied the data as a hex dump and used (CyberChef)[https://gchq.github.io/CyberChef/] to convert it to a viewable image.
<img width="958" height="332" alt="image" src="https://github.com/user-attachments/assets/b0057df1-60f3-4f1f-8123-44e3a805ec4f" />

The image itself wasnt that intresting, but then I remembered to check exif data. I visited a site that allowed me to view it and found something quite strange

<img width="1111" height="57" alt="image" src="https://github.com/user-attachments/assets/babaeef3-6552-46bf-98d4-fd1dff4d284d" />

Base64 decoding it reveals the flag

<img width="685" height="615" alt="image" src="https://github.com/user-attachments/assets/343af41f-ca22-4554-93dd-d2d978e3f9f6" />

# breaking-zip
```
This zip archive is impossible to unzip, therefore it's impossible to get the flag.
Source?
Just trust me bro.
```
I firstly opened the zip in 7-Zip and saw the following file structure.
<img width="837" height="191" alt="image" src="https://github.com/user-attachments/assets/8d662f12-83d9-47ef-88fa-c1c6733d181d" />

Googling around I found that most of these files are from `https://github.com/adryd325/oneko.js/`. I found a program called PKCrack that can decrypt a zip if one of its file contents are in plain-text. I downloaded the exe and used the params `pkcrack -C breaking_zip.zip -c oneko.js/oneko.gif -P oneko.zip -p oneko.gif -d decrypted.zip`, oneko.zip containing the "oneko.gif" file

<img width="1089" height="417" alt="image" src="https://github.com/user-attachments/assets/63b88966-c71b-4add-adcb-4ce0a908520a" />

SUCCESS!!!! Opening flag.txt reveals it

<img width="409" height="91" alt="image" src="https://github.com/user-attachments/assets/d6d85b65-ede9-4c15-b9f0-32d4460e8dc2" />

# Open Gallery - text only version
```
the note wall accepts printable raw notes with no extension, or printable .txt files

get flag from /flag.txt
```
This version was a lot stricter, but it still had flaws. It allowed me to upload a .htaccess file [`AddType application/x-httpd-php .txt`] that made every .txt file behave like a .php. It was the same proccess as before

<img width="986" height="910" alt="image" src="https://github.com/user-attachments/assets/293d8ee4-305d-4fe6-9bb5-5d13541f6828" />

# movie-proxy
```
MovieTalk 2010 is a tiny public forum for proxying movie reviews and box office guesses.
```
I went to the website and noticed that the reviews page had some internal talk, specifically about forward-user.
<img width="885" height="476" alt="image" src="https://github.com/user-attachments/assets/31c9bb28-e0fb-4d8d-af76-304db092acf1" />

I went to the internal page and noticed this.
<img width="1021" height="362" alt="image" src="https://github.com/user-attachments/assets/50b05eb3-3e3b-43f7-8004-a95152eb18eb" />

I copied the request as fetch and added the "X-Forwarded-User" header.
<img width="753" height="255" alt="image" src="https://github.com/user-attachments/assets/e91aebd7-b6a2-4143-90ca-0e79916fc3cf" />

And we got the flag

<img width="833" height="519" alt="image" src="https://github.com/user-attachments/assets/5fbc3424-3e3b-4646-b773-e77db665000f" />

# Front Desk
```
the public desk counts bytes
Get to the restricted localhost endpoint, /admin/flag !
```
I opened the site and was informed that there was an public desk, aswell as one that was internal.
<img width="1160" height="610" alt="image" src="https://github.com/user-attachments/assets/1d1caacf-8c0d-4357-986f-861a1681e935" />

Clicking on the submit button revealed nothing else.
<img width="1150" height="426" alt="image" src="https://github.com/user-attachments/assets/9f8956e6-d39b-47c4-8ba1-24286bbd8b4a" />

I noticed that the server was using HTTP/1.1 which is known to be vulnerable to request smuggling
<img width="329" height="451" alt="image" src="https://github.com/user-attachments/assets/0d2891d9-7732-4036-b30e-e616dd49ac56" />

I duplicated the submit POST request in Burp Suite and added content that can be interpreted as a request to localhost.
```
POST /submit HTTP/1.1
Host: 194.102.62.183:22622
Content-Type: application/x-www-form-urlencoded
Content-Length: 50
Transfer-Encoding: chunked

0

GET /admin/flag HTTP/1.1
Host: localhost
```
Success.

<img width="618" height="623" alt="image" src="https://github.com/user-attachments/assets/d6bd644d-15a2-49be-8299-9b30f93293c3" />

# storage gateway
```
During an internal audit, a storage gateway was discovered on port 23 along with some credentials: analyst:zeroday2026!

Further investigation suggests that sensitive data is stored in an archive under a different account.
```
Using telnet I connected to the ip and port and logged into the acount
<img width="1101" height="390" alt="image" src="https://github.com/user-attachments/assets/a2bf777b-028a-4182-be89-dd80a5be318f" />
I went to the root and noticed a file called `startup.sh`, I then listed it
<img width="1039" height="494" alt="image" src="https://github.com/user-attachments/assets/b3968371-b974-44f5-af74-938583fefe8c" />
Great success.

