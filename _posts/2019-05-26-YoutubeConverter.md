---
title: "Convert Youtube videos into mp3 using Python"
author_profile: true
tags: [Computer]
---

<p align="justify"> 
This is a short explanation of how to use this 
<a href="https://github.com/JLefortBesnard/YoutubeConverter">Python script</a>
to download Youtube videos and convert them into mp3.
</p>


## 1. Ipython + needed packages installed
<p align="justify"> 
First you need to have ipython 3 installed (Python 3 + ipython). How to install it is beyond the scope of this post but you can find information <a href="http://jeremylefortbesnard.de/LearnPythonandML/">there</a>.
</p>

Once installed, you need to have a few packages installed. 

To install them, activate ipython (open your terminal and type ipython) and type:

```
!pip install pytube
!pip install moviepy
!pip install subprocess
```
<p align="justify"> 
The ! before the command is to run the command outside Python.
The other packages should already be coming with Python. If not, just follow the same idea: 
</p>

!pip install _package-name_

  
## 2. Download the youtube converter Python script
<p align="justify">
Once the installation of ipython and packages is done, you can download the script "youtube_converter.py" <a href="https://github.com/JLefortBesnard/YoutubeConverter">there</a> on your Desktop.
</p>

Click on "Clone or Download" on the Github page, and select "Download ZIP"
<p align="justify"> 
Extract the zip and in the extracted folder, you will find the file "Youtube_converter.py".
Cut and paste it on your Desktop.
</p>

## 3. Run the program

Ok, we are almost done.

<p align="justify">
In your terminal, still with ipython activated, left click on the file "youtube_converter.py" you downloaded and on your terminal, type "run " (mind the space after run) and paste the selection after the space. The line should look similarly:
</p>

```
run /Desktop/youtube_converter.py
```

<p align="justify"> 
The program will ask you to check if you want to create the music folder in the current path or in another path.
Type 0 and press enter to create the folder music in the current path (the mp3 will be converted there).
Type 1 and press enter if you want to define another destination for the folder music.
</p>

Alright, so now, the program asks you to paste the Youtube URL one by one. Feel free to add as many urls as you like.

Once your done, type 1 and press Enter.

## 4. Enjoy the output!
<p align="justify"> 
That's it. Now you just have to wait until your computer does the work. 
Go to the music folder to listen to the output!
</p>


