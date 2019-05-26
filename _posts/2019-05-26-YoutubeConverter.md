---
title: "Convert Youtube videos into mp3 using Python"
author_profile: true
tags: [Computer]
---

This is a short explanation of how to use this 
[Python script]("https://github.com/JLefortBesnard/YoutubeConverter/blob/master/youtubemp3.py") 
to download Youtube videos and convert them into mp3.

First you need to have Python 3 installed. How to install it is beyond the scope of this post but you can find information 
[there]("https://github.com/JLefortBesnard/Learn-python-and-machine-learning/wiki/Tips-for-learning-Python-and-Machine-Learning").
Once installed, you need to have a few packages installed. Activate Python and type in you terminal:

```
!pip install pytube
!pip install moviepy
!pip install subprocess
!pip install ipython
```

The ! before the command is for doing the command outside Python.
The other packages should already be coming with Python. If not, just follow the same idea: !pip install ...

Once this is done, you must create a folder named "music" in you Desktop.You could do this using Python as well.

```
path = 'Desktop\music' 
if not os.path.exists(path):
    os.makedirs(path)
```  

Then you can paste the first part of the script until os.chdir("Desktop\\music").
This command directs the terminal into the folder music.

The next step is to copy all the URL inside a list as below:

```
# paste here the Youtube URL you wanna convert
urls = ["https://www.youtube.com/watch?v=NlUQbrlb2iQ",
        "https://www.youtube.com/watch?v=3V1VwEKFe0g"]
```
Mind the inverted commas and the squared brackets as well as the indentation. The format is very important in Python.

Once this is all set you can copy paste the rest of the script in your terminal.
