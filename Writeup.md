# consent-kiosk
When I opened the website, the first thing I noticed was the "I agree" button avoiding the mouse.
<img width="773" height="494" alt="image" src="https://github.com/user-attachments/assets/ab67f5f1-7c67-4b2a-920d-3c71cd9cc3fd" />

I opened the console right after, and the website detected it, didin't take me too long to notice that the detection could be bypassed by refreshing with the console open
<img width="1918" height="918" alt="image" src="https://github.com/user-attachments/assets/719c0bbe-3102-4a93-945c-d421445ace29" />

When I checked the network requests, I noticed a file called "telemetry.js"
<img width="837" height="513" alt="image" src="https://github.com/user-attachments/assets/d29596da-98c8-4357-87bb-0684397178d6" />

I copied its content to the console, and called the function directly.
<img width="1919" height="910" alt="image" src="https://github.com/user-attachments/assets/7dc81eb8-c62f-4b8e-88f3-fadf623aa5ad" />

# legacy-profile
After I registered to the website, I noticed a session token was created that had no valid signature.
<img width="659" height="196" alt="image" src="https://github.com/user-attachments/assets/3d2d6086-a1de-4f6e-b272-f2f971e959ed" />

I visited a JWT debugging website (jwt.io) and changed my roles to become an admin.
<img width="1223" height="855" alt="image" src="https://github.com/user-attachments/assets/90c9aed7-058b-4837-b482-dcd5e9b619bf" />

I removed the signature part of my alterned one and replaced it with "legacy-signature". Then I visited the admin page.
<img width="1020" height="358" alt="image" src="https://github.com/user-attachments/assets/5997e4bc-d4d7-4499-a18f-a84d0de8ec3b" />

# Open Gallery
Instantly I noticed that the website allowed any file extensions to be uploaded. Noticing the "PHP" headers, I uploaded a small php that could ls and cat each file

<img width="589" height="306" alt="image" src="https://github.com/user-attachments/assets/90c99b36-c18b-47ee-bca7-db28528e25b0" />

After visiting my submission, I was able to get the flag from the root
<img width="968" height="925" alt="image" src="https://github.com/user-attachments/assets/524de7db-e12d-4d3e-9e16-fae7689a542a" />

# MacroPlex
After opening the .eml file in Outlook, I instantly knew the first 2 questions required to solve the challange.
<img width="1416" height="256" alt="image" src="https://github.com/user-attachments/assets/ff2d45f5-02c3-4ade-b14c-51b9187ecd7f" />

Opening the .docm file in Libreoffice, I got informed that the file had macros.
<img width="1431" height="741" alt="image" src="https://github.com/user-attachments/assets/044258cc-05e0-4706-a240-6c1363cb42e8" />

Viewing the macro, I got the answer to the third question
<img width="1422" height="741" alt="image" src="https://github.com/user-attachments/assets/3af15604-f294-4212-926c-a45ec2d75094" />

The flag was: `ZDTM{Mara.M@macroplex.com_docm_m4lw4re}`

# in-plain-sight
I opened the pcap file in Wireshark, and noticed a perculiar response to a request containing a jpeg image
<img width="1919" height="1037" alt="image" src="https://github.com/user-attachments/assets/88d87851-a370-47a7-83b4-31632dc7ef97" />

I copied the data as a hex dump and went to cyberchef to convert it to a viewable image.
<img width="958" height="332" alt="image" src="https://github.com/user-attachments/assets/b0057df1-60f3-4f1f-8123-44e3a805ec4f" />

The image wasnt that intresting, until I remembered about exif data. I visited one that allowed me to view it and found something quite strange

<img width="1111" height="57" alt="image" src="https://github.com/user-attachments/assets/babaeef3-6552-46bf-98d4-fd1dff4d284d" />

Base64 decoding it gets us the flag

<img width="685" height="615" alt="image" src="https://github.com/user-attachments/assets/343af41f-ca22-4554-93dd-d2d978e3f9f6" />

# breaking-zip

I firstly opened the zip in 7z, and I saw this file structure.
<img width="837" height="191" alt="image" src="https://github.com/user-attachments/assets/8d662f12-83d9-47ef-88fa-c1c6733d181d" />

Googling around I found that most of these files are from `https://github.com/adryd325/oneko.js/`. After searching around I found a program called PKCrack that can decrypt a zip if one of its file contents are in plain-text. I downloaded the exe and used the params `pkcrack -C breaking_zip.zip -c oneko.js/oneko.gif -P oneko.zip -p oneko.gif -d decrypted.zip`, oneko.zip containing the "oneko.gif" file

<img width="1089" height="417" alt="image" src="https://github.com/user-attachments/assets/63b88966-c71b-4add-adcb-4ce0a908520a" />

SUCCESS!!!! Opening flag.txt reveals it

<img width="409" height="91" alt="image" src="https://github.com/user-attachments/assets/d6d85b65-ede9-4c15-b9f0-32d4460e8dc2" />

