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
<img width="968" height="925" alt="image" src="https://github.com/user-attachments/assets/461f3012-95ae-4271-934b-c36ee7263214" />
