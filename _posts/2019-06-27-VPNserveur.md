---
title: "How to ssh connect to a linux server with a windows machine"
author_profile: true
tags: [Computer]
---

Let's say you have a Windows machine (Windows 10) and you want to remotely connect to a Linux server.

## Main ideas
<p align="justify">
You might need to VPN (virtual private network) to connect to the network domain of your university before connecting to the server. 
</p>
Most universities ask labs to use a VPN to configure a lab server (to make it more secure).

You can see a VPN as a secure door on top of the door to connect to the server. 

Once VPN connected, you can remotely connect to the server. A server is basically another computer.

Once connected, it's like having another computer at your disposal.

You might need to transfer files from your local computer to the server or to use an app (installed on the server) on your local machine.

If your operating system is Windows (here 10) and you are connecting to a Linux server, this can be tricky.

Below are some tips I found to make it work.

## Configure the VPN

<p align="justify">
Your lab should give you some information such as VPN ip, VPN name and VPN passport. You will need these informations to VPN connect.
Open the network & internet settings, click on VPN, add a VPN connection and then fill in the information.
</p>
<p align="justify">
Once done, connect to the VPN: click on the network logo at the bottom of your Windows desktop, you will find the newly added VPN name.
Just click on it. It should automatically connect.
</p>
Open your terminal console and type in:

```
ssh username@serveraddress -p port
```

<p align="justify">
Replace username, serveraddress, and port (port is usually 22) with the proper information that your lab should have given to you.
Then, you will be asked to enter your password. No worries if nothing is happening while you're typing your password in, that's normal, just type it and press enter.
</p>
That's it, you are now connected to the server!

## Using a server app (1)

So you are connected. That's great. Now let's try to open an app already installed in the server, let's say Spyder (this was true for me).
You type in spyder on your terminal and you got QXcb error...

Okay, let's fix this, open your favorite webbrowser.

Wait, oh nooo, c...

## Internet connection while using the VPN connection.

Internet is not working anymore because the VPN connection is used as default. 
<p align="justify">
Open the network&internet settings, click on VPN, you will see the status of your VPN connection.
Click on Change adapter options. Right click on the VPN you just configured, select properties. Click on the tab Networking, select the line internet Protocol Version 4 (TCP/IPv4) and click on properties.
Then, click on Advanced and unpick the Use default gateway on remote network. Click ok, that's it, your internet connection should be back on track. 
If not, try disconnect VPN, check that you have internet back and then reconnect VPN.
</p>

## Using a server app (2)

Ok, now that you have internet back, let's fix this QXcb problem. Follow the procedure writen 
<a href="http://www.geo.mtu.edu/geoschem/docs/putty_install.html">there</a>.

In sum, download, install & configure putty as well as Xming. Everything is pretty straightforward if you folow the procedure from the above website.

<p align="justify">
Once everything is done, remember to save the configuration on putty. Then you just have to load and open a session. A terminal screen will open and ask for your password. Now, 
just type in the name of the already installled app you wanna use (e.g., spyder) and the app will open on your local computer.
</p>

## Transfering files
<p align="justify">
Okay, great, you are connected to the server, you can still connected to the internet and you can use apps installed on the server. What about transfering files from your local PC to the server and vice et versa?
</p>

### Using Filezilla

<p align="justify">
Filezilla is a great software that allows you to transfer files between your PC and the server. Download and install <a href="https://filezilla-project.org/">Filezilla Server</a>.
Once installed, open it and enter the server address in Host, your username in the usernam tab, your password and the Port, then click on Quick connect.
</p>
<p align="justify">
That's it, you're connected and you can now exchange file. On the left side are your local Desktop folders, on the right side are the server folders. You just have to click on stuff you want to transfer. The file to copy is the one you are clicking on and the destination folder is the one you are in on the other side.
</p>

### Using the scp command

If you want to transfer files directly from your terminal, use the scp command.

Connect to the VPN, open your terminal, and type in:

```
scp file_to_copy_from_local_computer.txt username@serveraddress:/destination_path
```
for example: scp my_text.txt jeremy@195.225.114.1:/home/helloworld

If the port is not 22, type in you port number after a capital P:

```
scp -P port file_to_copy_from_local_computer.txt username@serveraddress:/destination_path
```

If you need to copy a folder:

```
scp -P port -r folder_to_copy_from_local_computer.txt username@serveraddress:/destination_path
```

The -r stands for recursively, meaning that everything inside the folder will be copied

FYI, to copy from the server to your local machine, use this form:
```
scp -P port username@serveraddress:/path_file_to_send /path_where_to_put
```

Hope this help. 




