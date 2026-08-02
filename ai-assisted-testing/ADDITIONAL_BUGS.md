[AI-assisted]_BUG_1

Title: Failed to upload the background image for the new album.
Description: I tried to create a new album, but when uploading the background image, I couldn't save it because the app kept telling me the name was already taken, no matter which name I chose.
Severity: Critical
Priority: High

Steps to reproduce:
1. Log into the application with an existing user.
2. Go to the page: "http://demo.baasic.com/angular/starterkit-photo-gallery/album/create". 
3. Type into "Album Name" textbox: Summer094129041
4. Type into "Description" textbox: Summer094129041
5. CLick on button: "SAVE ALBUM"
6. Click on "Click to upload Cover Image"
7. Type into "Photo Name" textbox: Summer094129041
8. Type into "Description" textbox: Summer094129041
9. Click on "Upload Image"
10. Select an image stored on your device. 
11. Click on "UPLOAD" button. 
12. Wait for the application to process the request, this can take about half a minute. 
13. Find the error under "Photo Name" text box: "Name taken, please choose another."

Expected result: Album Cover Image sucessfuly uploaded. 
Actual result: Upload failed with an error message, "Name taken, please choose another."
Environment: Windows 11, Android version 16
Attachments: "Mono/manual-testing/screenshots/bug_1"

-------------------------------
-------------------------------
