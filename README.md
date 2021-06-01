# webdl

## 1) Preparation and installation


1. Download these files:

        https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-full.7z
        https://youtube-dl.org/downloads/latest/youtube-dl.exe

2. Create a new folder into which we are going to extract the exe files, kinda like an install folder

3. Into this folder copy the downloaded youtube-dl.exe 

4. In the ffmpeg-release-full.7z archive there is a bin folder, copy the 3 .exe files (ffmpeg, ffplay, ffprobe) into the new directory you created in Step 2

**Optional part of Step 1 (if you do this you will be able to run youtube-dl from any folder):**

5. Open up start menu and search for Environment variable and open up the first hit

6. On the popup window make sure you re on the Special tab and at the bottom click on Environment variables

7. On the upper part of the new popup windows search for the Variable names Path, click on it twice to edit

8. Click on Browse and navigate the files browser to the folder you created in Step 2, then click on Ok

9. Now click Ok three more times to close all the windows, now we are ready with this step!

## 2A) Getting the stream link via extension


1. Install this in Firefox, https://addons.mozilla.org/en-US/firefox/addon/hls-stream-detector/ it will give you the stream link

2. Ready to proceed to step 3.

## 2B) Getting the stream link manually 

1. On the video page open up the Developer Tools with F12 in Chrome of Firefox

2. Click on the network tab

3. Reload the page, start the livestream, after it starts playing you can pause it for the time being

4. Now this Network tab shows the traffic between the website and your computer

You will have to try out these substeps to determine which livestream the page is doing:

### A) m3u8

5A. There will be a small textbox on the left you have to enter m3u8 into it and one result will remain

6A. Click on it this will bring up a new window in the right

7A. Click on the new windows's Header tab and copy the Request URL

8A. Succes, now you have the stream link!

### B) mpd

5B. There will be a small textbox on the left you have to enter mpd into it and one result will remain

6B. Click on it this will bring up a new window in the right

7B. Click on the new windows's Preview or Response tab, check the video qualities listed and copy the URL

8B. Succes, now you have the stream link!

### C) master.json

5C. There will be a small textbox on the left you have to enter master.json into it and one result will remain

6C. Click on it this will bring up a new window in the right

7C. Click on the new windows's Header tab and copy the Request URL

8C. Delete the json?base64_init=1 part of the copied link and replace it with m3u8 so you end up with master.m3u8

8C. Succes, now you have the stream link!

## 3) Usage


1. In the folder where the four .exe files are (youtube-dl, ffmpeg, ffplay, ffprobe) hold Shift and right click (if you completed the optional part of Step 1, any folder will do)

2. From the popup select 'Open Powershell window here'

3. This will bring up a Powershell windows with the path to your folder

4. Into this you will have to enter, the streamlink is what you copied from the Developer Tools:

        youtube-dl streamlink

5. Also if you want to be extra careful, put the streamlink between paranthesis like this:

        youtube-dl "streamlink"
        
6. Press enter and the grabbing process will start!
