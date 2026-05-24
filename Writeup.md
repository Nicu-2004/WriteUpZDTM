# consent-kiosk
When I opened the website, the first thing I noticed was the "I agree" button avoiding the mouse.
<img width="773" height="494" alt="image" src="https://github.com/user-attachments/assets/ab67f5f1-7c67-4b2a-920d-3c71cd9cc3fd" />

I opened the console right after, and the website detected it. It didin't take me long to notice that the detection could be bypassed by refreshing the page with the console already open.
<img width="1918" height="918" alt="image" src="https://github.com/user-attachments/assets/719c0bbe-3102-4a93-945c-d421445ace29" />

When I checked the network requests, I noticed a file called `telemetry.js`.
<img width="837" height="513" alt="image" src="https://github.com/user-attachments/assets/d29596da-98c8-4357-87bb-0684397178d6" />

I copied its content to the console, and called the function directly.
<img width="1919" height="910" alt="image" src="https://github.com/user-attachments/assets/7dc81eb8-c62f-4b8e-88f3-fadf623aa5ad" />

# legacy-profile
After I registered to the website, I noticed that a session token was created that had no valid signature.
<img width="659" height="196" alt="image" src="https://github.com/user-attachments/assets/3d2d6086-a1de-4f6e-b272-f2f971e959ed" />

I visited a JWT debugging website ([jwt.io](https://jwt.io)) and changed my roles to become an admin.
<img width="1223" height="855" alt="image" src="https://github.com/user-attachments/assets/90c9aed7-058b-4837-b482-dcd5e9b619bf" />

I removed the signature part of my alterned one and replaced it with `legacy-signature`. Then I visited the admin page.
<img width="1020" height="358" alt="image" src="https://github.com/user-attachments/assets/5997e4bc-d4d7-4499-a18f-a84d0de8ec3b" />

# Open Gallery
I instantly noticed that the website allowed files with any extension to be uploaded. Noticing the PHP headers, I uploaded a small PHP file that could ls and cat each file

<img width="589" height="306" alt="image" src="https://github.com/user-attachments/assets/90c99b36-c18b-47ee-bca7-db28528e25b0" />

After visiting my submission, I was able to get the flag from the root directory.
<img width="968" height="925" alt="image" src="https://github.com/user-attachments/assets/524de7db-e12d-4d3e-9e16-fae7689a542a" />

# MacroPlex
After opening the .eml file in Outlook, I instantly knew the first 2 questions required to solve the challange.
<img width="1416" height="256" alt="image" src="https://github.com/user-attachments/assets/ff2d45f5-02c3-4ade-b14c-51b9187ecd7f" />

Opening the .docm file in Libreoffice, I got informed that the file contained macros.
<img width="1431" height="741" alt="image" src="https://github.com/user-attachments/assets/044258cc-05e0-4706-a240-6c1363cb42e8" />

Viewing the macro gave me the answer to the third question
<img width="1422" height="741" alt="image" src="https://github.com/user-attachments/assets/3af15604-f294-4212-926c-a45ec2d75094" />

The flag was: `ZDTM{Mara.M@macroplex.com_docm_m4lw4re}`

# in-plain-sight
I opened the pcap file in Wireshark, and noticed a peculiar response to a request containing a jpeg image
<img width="1919" height="1037" alt="image" src="https://github.com/user-attachments/assets/88d87851-a370-47a7-83b4-31632dc7ef97" />

I copied the data as a hex dump and used (CyberChef)[https://gchq.github.io/CyberChef/] to convert it to a viewable image.
<img width="958" height="332" alt="image" src="https://github.com/user-attachments/assets/b0057df1-60f3-4f1f-8123-44e3a805ec4f" />

The image itself wasnt that intresting, but then I remembered to check exif data. I visited a site that allowed me to view it and found something quite strange

<img width="1111" height="57" alt="image" src="https://github.com/user-attachments/assets/babaeef3-6552-46bf-98d4-fd1dff4d284d" />

Base64 decoding it reveals the flag

<img width="685" height="615" alt="image" src="https://github.com/user-attachments/assets/343af41f-ca22-4554-93dd-d2d978e3f9f6" />

# breaking-zip

I firstly opened the zip in 7-Zip and saw the following file structure.
<img width="837" height="191" alt="image" src="https://github.com/user-attachments/assets/8d662f12-83d9-47ef-88fa-c1c6733d181d" />

Googling around I found that most of these files are from `https://github.com/adryd325/oneko.js/`. I found a program called PKCrack that can decrypt a zip if one of its file contents are in plain-text. I downloaded the exe and used the params `pkcrack -C breaking_zip.zip -c oneko.js/oneko.gif -P oneko.zip -p oneko.gif -d decrypted.zip`, oneko.zip containing the "oneko.gif" file

<img width="1089" height="417" alt="image" src="https://github.com/user-attachments/assets/63b88966-c71b-4add-adcb-4ce0a908520a" />

SUCCESS!!!! Opening flag.txt reveals it

<img width="409" height="91" alt="image" src="https://github.com/user-attachments/assets/d6d85b65-ede9-4c15-b9f0-32d4460e8dc2" />

# Open Gallery - text only version 
This version was a lot stricter, but it still had flaws. It allowed me to upload a .htaccess file [`AddType application/x-httpd-php .txt`] that made every .txt file behave like a .php. It was the same proccess as before

<img width="986" height="910" alt="image" src="https://github.com/user-attachments/assets/293d8ee4-305d-4fe6-9bb5-5d13541f6828" />

# movie-proxy
I went to the website and noticed that the reviews page had some internal talk, specifically about forward-user.
<img width="885" height="476" alt="image" src="https://github.com/user-attachments/assets/31c9bb28-e0fb-4d8d-af76-304db092acf1" />

I went to the internal page and noticed this.
<img width="1021" height="362" alt="image" src="https://github.com/user-attachments/assets/50b05eb3-3e3b-43f7-8004-a95152eb18eb" />

I copied the request as fetch and added the "X-Forwarded-User" header.
<img width="753" height="255" alt="image" src="https://github.com/user-attachments/assets/e91aebd7-b6a2-4143-90ca-0e79916fc3cf" />

And we got the flag

<img width="833" height="519" alt="image" src="https://github.com/user-attachments/assets/5fbc3424-3e3b-4646-b773-e77db665000f" />

# Front Desk
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
