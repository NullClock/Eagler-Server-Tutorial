# How to make an Eaglercraft server:<br> A Comprehensive tutorial
So you want to make an [Eaglercraft](https://eaglercraft.com/) server? That's great. I'm here to help!<br>
Every server version has a slightly different process and all of them will be properly described here. As of April 2025, there are 3 major versions:

 - 1.12.2
 - 1.8.8
 - 1.5.2
> [!NOTE]
> 1.5.2 is the first ever Eaglercraft version, and 1.8.8 is the second and both are officially endorsed by lax1dude. All version above or below any of those two are unofficial and are not supported (with an exception for 1.12.2).

Alright, let's get to it. Here are some requirements for your server:
 - A machine with AT LEAST 4 GB of memory (RAM)
 - At least 10GB storage
 - Access to the file system and executing jar files
 - Either:
   1. A Domain with Cloudflare Nameservers OR
   2. An [ngrok](https://ngrok.com/) account

###  Install ngrok:
**Windows**: Open command prompt and run ``choco install ngrok``<br>
**Debian Linux**: Open your terminal and run 
```
curl -sSL https://ngrok-agent.s3.amazonaws.com/ngrok.asc \
  | sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null \
  && echo "deb https://ngrok-agent.s3.amazonaws.com buster main" \
  | sudo tee /etc/apt/sources.list.d/ngrok.list \
  && sudo apt update \
  && sudo apt install ngrok```<br>
```
**MacOS**: Open your terminal and run ``brew install ngrok``

Done? Alright. So, first things first, we need to set up the actual (©) Minecraft server software, which for this tutorial we will use PaperMC, with a nice alternative being Cuberite. <br>
Click the respective version to go to their section: <br>
[1.12.2 Server](#creating-a-1.12.2-server),  [1.8.8 Server](#creating-a-1.8.8-server),  [1.5.2 Server](#creating-a-1.5.2-server)

## Creating a 1.12.2 Server
Go to the [all builds page](https://papermc.io/downloads/all) at [papermc.io](https://papermc.io) and find 1.12.2 in the sidebar, and make sure you're getting build #1620. The file should download into your computer. Make sure to put the ``.jar`` file into its own folder or else your Desktop/Downloads folder will get really cluttered and things will be hard to find. When you've done that, make sure you have Java 11 or higher installed, and run the file! You'll see the folder start to populate with files and the server will eventually exit, telling you to accept the EULA to continue. Go into eula.txt and change whatever's after the ``=`` to ``true``. Now, run the ``.jar`` file again.<br><br>
By this point, you already have a basic server running **BUT** without Eaglercraft support and only accessible to other people on your Wi-Fi. What you need to do now is open the ``server.properties`` file in your server files and find ``online-mode`` and set it to ``false``, this will make your server cracked, so later on you'll probably want to get either of the ``AuthMe``, ``nLogin`` or ``LoginSecurity`` plugins. Now finally restart your server, and don't close it so that we can move onto installing BungeeCord.
#### Installing BungeeCord:
Okay, now, we can get Bungee from by going to [this](http://ci.md-5.net/job/BungeeCord/) link and clicking on ``BungeeCord.jar``. Move BungeeCord into a SEPARATE FOLDER DIFFERENT THAN THE FOLDER THAT YOUR PAPER SERVER IS IN! Now open ``BungeeCord.jar`` and it'll open another terminal, but with your Bungee stuff. After a few seconds with the server opened, there should be a ``config.yml`` file and a ``plugins`` folder in the Bungee folder  and we'll be needing to add the Eaglercraft plugin, as well as disabling ``online_mode`` in the ``config.yml`` file. Open the ``config.yml`` file in the folder, and find the ``online_mode`` property, now, change it to ``false``. Done? Okay. now we need to add the EaglercraftXBungee plugin to BungeeCord. You can download it from Spigot at [this](https://www.spigotmc.org/resources/eaglerxbungee.120857/reviews) link or get the OFFICIAL release at [this other](https://github.com/lax1dude/eagl3rxbungee) link.
<br><br>
 When you download the file, move it to the ``plugins`` folder in your bungeecord stuff, restart your server and leave it open, make sure your paper server is up too. You can't close the terminal/command prompt popups or your server will go down.
Now, finally we need to port forward with ngrok! This should be easy and you'll need your ngrok account. Go to [dashboard.ngrok.com](https://dashboard.ngrok.com), choose your OS, and copy the 2 last commands, and finally run it in a new/spearate terminal or command prompt, but replace the 8080 in the last command with 8081 for eagler. If you want java support, run the last commands AGAIN in another terminal, but change 8080 to 25565 instead. You can either: choose a custom link in the ngrok dashboard, get a random one when you run the command, or link your own domain in the ngrok dashboard. Now, FINALLY, you can join your server by either pasting the link (remove the https!) in Eaglercraft or pasting the second link in Java 1.12.2!
## Creating a 1.8.8 Server
This section describes the process of making a publicly accessible EaglercraftX server.
#### Getting Started:
First things first, we'll need the PaperMC 1.8.8 jarfile, if you want an alternative I would recommend Cuberite. Go to [the PaperMC build explorer](https://papermc.io/downloads/all) and find 1.8.8 in the sidebar and download build #445. When downloaded, make sure you take the file into a separate folder or else when you run the ``.jar`` file, it'll extract everything into your downloads/desktop folder and that'll be a pain in the a\*\* to deal with. After that, make sure you have Java **8** (it needs to be Java 8 specifically) if you don't have it you can just search it up and download the installer. Run the ``.jar`` file and it should start to popular the folder with files. Now, go into the folder, open ``eula.txt`` and set everything after ``=`` to ``true``. Run your server again and it should add a ``server.properties`` file to the folder within a few seconds. Open that file and set the ``online-mode`` setting to ``false`` and restart your server. This will make your server cracked, and there's no way to avoid that, so later on you'll probably want to get either of the ``AuthMe``, ``nLogin`` or ``LoginSecurity`` plugins. Now finally restart your server, and don't close it so that we can move onto installing BungeeCordw	8

#### Installing BungeeCord:
Okay, now, we can get Bungee from by going to [this](http://ci.md-5.net/job/BungeeCord/) link and clicking on ``BungeeCord.jar``. Move BungeeCord into a SEPARATE FOLDER DIFFERENT THAN THE FOLDER THAT YOUR PAPER SERVER IS IN! Now open ``BungeeCord.jar`` and it'll open another terminal, but with your Bungee stuff. After a few seconds with the server opened, there should be a ``config.yml`` file and a ``plugins`` folder in the Bungee folder  and we'll be needing to add the Eaglercraft plugin, as well as disabling ``online_mode`` in the ``config.yml`` file. Open the ``config.yml`` file in the folder, and find the ``online_mode`` property, now, change it to ``false``. Done? Okay. now we need to add the EaglercraftXBungee plugin to BungeeCord. You can download it from Spigot at [this](https://www.spigotmc.org/resources/eaglerxbungee.120857/reviews) link or get the OFFICIAL release at [this other](https://github.com/lax1dude/eagl3rxbungee) link.
<br><br>
 When you download the file, move it to the ``plugins`` folder in your bungeecord stuff, restart your server and leave it open, make sure your paper server is up too. You can't close the terminal/command prompt popups or your server will go down.
Now, finally we need to port forward with ngrok! This should be easy and you'll need your ngrok account. Go to [dashboard.ngrok.com](https://dashboard.ngrok.com), choose your OS, and copy the 2 last commands, and finally run it in a new/spearate terminal or command prompt, but replace the 8080 in the last command with 8081 for eagler. If you want java support, run the last commands AGAIN in another terminal, but change 8080 to 25565 instead. You can either: choose a custom link in the ngrok dashboard, get a random one when you run the command, or link your own domain in the ngrok dashboard. Now, FINALLY, you can join your server by either pasting the link (remove the https!) in Eaglercraft or pasting the second link in Java 1.8.8!

## Creating a 1.5.2 Server
W.I.P (I'm lazy to complete this lol)

![Alt](https://repobeats.axiom.co/api/embed/4df69500cea39a61868156d07b7ac419713826c6.svg "Repobeats analytics image")
