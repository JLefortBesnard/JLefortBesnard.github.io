---
title: "Convert Youtube videos into mp3 using Python"
author_profile: true
tags: [Computer]
---

<p align="justify"> 
This is a short explanation of how to use this
<a href="https://github.com/JLefortBesnard/YoutubeConverter">Python script</a>
to download Youtube videos and convert them into mp3. The idea is that you run this script while scrolling on Youtube videos and copy-paste the URL of each video you find interesting as you go.
</p>


## 1. Ipython + needed packages installed
<p align="justify"> 
First you need to have ipython 3 installed (Python 3 + ipython). How to install it is beyond the scope of this post but you can find information <a href="http://jeremylefortbesnard.de/LearnPythonandML/">there</a>.
</p>

Once installed, you need to have a few packages installed. 

To install them, launch ipython: open your terminal and type ipython, if correctly installed then the terminal should display the version of Python and IPython installed, and the following line should start with "In[1]". 

Once ipython is ready to be used, type the following in your terminal:

```
!pip install pytube
!pip install moviepy
```
<p align="justify"> 
The ! before the command is to run the command outside Python.
The other packages should already be coming with Python. If not, you will have an error message while running the program such as "ModuleNotFoundError: No module named [...]". Then, simply follow the same idea to install it: 
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
In your terminal, still with ipython activated (see above), select the file "youtube_converter.py" and drop it on your terminal (this should give you the whole file path), type "run " (mind the space after run) before the complete path. The line should look similarly (depending on your OS and path structure):
</p>

```
run /User/Desktop/youtube_converter.py
```
<p align="justify"> 
Alright, so now, the program will first ask you to paste Youtube URL one by one. So pick a Youtube URL, paste it and press Enter. Feel free to add as many urls as you like but always one by one.
</p>

Once your done, type 1 and press Enter.

<p align="justify"> 
The program will then ask you to check if you want to create the music folder in the current path or in another path.
Type 0 and press enter to create the folder music in the current path (which is writen above the question on your terminal), the mp3 will be converted in there.
Type 1 and press enter if you want to define another destination for the folder music. You will have to define the whole new path (not including music). For example, it could be something like user/Desktop/personal_stuff. Writing this path would create a folder music in the folder personal_stuff in your Desktop. Mind that depending on your system, you might have to write a longer path.
</p>



## 4. Enjoy the output!
<p align="justify"> 
That's it. Now you just have to wait until your computer does the work. 
Go to the music folder to listen to the output!
</p>

<p align="justify"> 
The program will ask you if you want to convert more videos, type 0 and press Enter to continue (the program will start again), just press Enter to stop.
</p>

Feel free to improve the code (pull request) or to fork it.

<p align="justify"> 
Edit: Some Youtube videos won't download. If so, try closing your terminal and running the program again. Make sure you're not messing up with the terminal path (play around with the [pwd or cd command](https://www.guru99.com/terminal-file-manager.html) to check it before running the script). I suggest you start downloading (type 1 instead of pasting a new url) after copying a few Youtube URLs. It can be frustrating to list a lot of URLs and then find out that they can't be converted eventually.
 </p>

