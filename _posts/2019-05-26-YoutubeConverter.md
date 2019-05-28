---
title: "Convert Youtube videos into mp3 using Python"
author_profile: true
tags: [Computer]
---

<p align="justify"> 

This is a short explanation of how to use this 
<a href="https://github.com/JLefortBesnard/YoutubeConverter">Python script</a>
to download Youtube videos and convert them into mp3.

First you need to have ipython 3 installed (Python 3 + ipython). How to install it is beyond the scope of this post but you can find information <a href="http://jeremylefortbesnard.de/LearnPythonandML/">there</a>.
Once installed, you need to have a few packages installed. 

To install them, activate ipython (open your terminal and type ipython) and type:

```
!pip install pytube
!pip install moviepy
!pip install subprocess
```

The ! before the command is to run the command outside Python.
The other packages should already be coming with Python. If not, just follow the same idea: 

!pip install _package-name_

Once this is done, you can download the script "youtubemp3_refactoring.py" <a href="https://github.com/JLefortBesnard/YoutubeConverter">there</a> on your Desktop.

Still with ipython activated on your terminal, left click on the file "youtubemp3_refactoring.py" you downloaded and on your terminal, type "run " and paste the selection after the space. The line should look similarly:

```
run Desktop/youtube_converter.py
```

The program will ask you to check if you want to create the music folder in the current path or in another path.
Type 0 and press enter to create the folder music in the current path (the mp3 will be converted there).
Type 1 and press enter if you want to define another destination for the folder music.

Alright, now, the program asks you to paste the Youtube URL one by one.

Once your done, type 1 and press Enter.

That's it. Go to the music folder to listen to the output!

</p>
