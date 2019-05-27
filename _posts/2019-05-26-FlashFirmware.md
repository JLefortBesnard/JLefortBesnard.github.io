---
title: "Flash the firmware using ODIN (Galaxy Tab S2 MT810)"
author_profile: true
tags: [Computer]
---

If you're reading this post I guess you also messed around with your tablet.
So now, you don't have any OS installed...

No worries, you can fix it hopefully. This happened to me and here is how I solved it for the Galaxy Tab S2 MT810.

First download the firmware for your Samsung tablet, here is the link for the 
<a href="https://www.sammobile.com/firmwares/galaxy-tab-s2/SM-T810/">Galaxy Tab S2 MT810</a>. 
You need the model number. To find mine, I just remembered the approximate date and the country in which I bought the tablet and 
picked the firmware with the closest description. The downloading process might take a few hours.
The file should look like this: "T810XXU2CPK1_T810DBT2CPK1_HOME.tar.md5".

Rename it without the ".md5", so that it looks like: "T810XXU2CPK1_T810DBT2CPK1_HOME.tar".

Then, download <a href="https://odindownload.com/">ODIN</a>. 
Odin is used to flash a custom recovery firmware image to a Samsung Android device. 
<a href="https://en.wikipedia.org/wiki/Odin_(firmware_flashing_software)">More info about ODIN</a>. 
Extract it and open ODIN3_v3.13.1.EXE. It looks like this:

<img src="{{ site.url }}{{ site.baseurl }}/images/odin.png" alt="odin">

I didn't but you might also need Samsung <a href="https://androidmtk.com/download-samsung-usb-drivers">USB drivers</a>.

Ok, you are all set, let's do this.

Boot your tablet into download mode by pressing and holding the power key + the volume down key + the home key until this screen appears:

<img src="{{ site.url }}{{ site.baseurl }}/images/download1.png" alt="download1">

Then press the volum up key again to boot into the download mode.

<img src="{{ site.url }}{{ site.baseurl }}/images/download2.png" alt="download2">

Connect your tablet to your computer.

Get back to ODIN on your computer. On the log windows, "Added!!" should be written.
Pick the "options" tab and check that only "Auto Reboot " and "F. Reset Time" are selected.

<img src="{{ site.url }}{{ site.baseurl }}/images/odin2.png" alt="odin2">

On the right , click on "AP" and find the Samsung firmware you dowloaded and renamed ("T810XXU2CPK1_T810DBT2CPK1_HOME.tar")

<img src="{{ site.url }}{{ site.baseurl }}/images/odin3.png" alt="odin3">

Click on Start and wait for the flash to be done.

That's it, congratulations!


