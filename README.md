# webdl

## 1) Preparation and installation


1. Download these files:

        https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-full.7z
        https://youtube-dl.org/downloads/latest/youtube-dl.exe

2. Create a new folder into which you are going to download the video

3. Into this folder copy the downloaded youtube-dl.exe 

4. In the ffmpeg-release-full.7z archive there is a bin folder, copy the 3 .exe files (ffmpeg, ffplay, ffprobe) into the new directory you created in Step 1

5. Done!

## 2) Getting the stream link


1. On the video page open up the Developer Tools with F12 in Chrome of Firefox

2. Click on the network tab

3. Reload the page, start the livestream, after it starts playing you can pause it for the time being

4. Now this Network tab shows the traffic between the website and your computer

5. You will have to try out these substeps to determine which livestream the page is doing

### A) m3u8

5A. There will be a small textbox on the left you have to enter m3u8 into it and one result will remain

6A. Click on it this will bring up a new window in the right

7A. Click on the new windows's Header tab and copy the Request URL

8A. Succes, now you have the stream link!

## 3) Usage


1. In the folder where the four .exe files are (youtube-dl, ffmpeg, ffplay, ffprobe) hold Shift and right click

2. From the popup select 'Open Powershell window here'

3. This will bring up a Powershell windows with the path to your folder

4. Into this you will have to enter, the streamlink is what you copied from the Developer Tools:

        youtube-dl streamlink

5. Also if you want to be extra careful, put the streamlink between paranthesis like this:

        youtube-dl "streamlink"
        
6. Press enter and the grabbing process will start!
