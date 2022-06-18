[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)

# Minecraft Java Pocket Server

Minecraft Java server for Android Tutorial
## Why?

Why not? It is cool hosting your own server on your own device. 😎
## Requirements

- [Termux](https://github.com/termux/termux-app/releases)
- [AnLinux](https://play.google.com/store/apps/details?id=exa.lnx.a&hl=en&gl=US)
- Atleast 3GB of Ram available (not talking about your total RAM)
- Good CPU i guess, cause lags sucks, just more than 1.5ghz is enough

## Installation

**Download** and **Install** both Termux and Anlinux, *click links above*.

### Install Ubuntu on your Android Device

Open Anlinux

Swipe from left and then tap Dashboard

![](https://cdn.discordapp.com/attachments/979918594982936646/987372802782928958/20220617_230655.jpg)

And tap **Choose**

Select Ubuntu and press **OK**

Now tap **Copy** and then **Launch**

You'll now redirected to Termux

### Termux Setup

Run this command:

```bash
  apt update
```

After finishing update, **Paste** the copied script by holding anywhere inside the bash shell and click enter.

![](https://cdn.discordapp.com/attachments/979918594982936646/987378225707626566/Screenshot_2022-06-17-23-26-58-61.jpg)

Termux will now start downloading Ubuntu and it will take 2-3 minutes to install it.

After Installation is done, **Paste** the following command to run Ubuntu
```bash
./start-ubuntu.sh
```
Now, you should see `root@localhost:~#` on Termux,
that means Ubuntu is running in your device.

![](https://cdn.discordapp.com/attachments/979918594982936646/987379873498689606/IMG_20220617_233459.jpg)

### Install Java Development Kit on Ubuntu

Run these commands:
```bash
apt update

apt-get install software-properties-common
```
![](https://cdn.discordapp.com/attachments/979918594982936646/987384317191815248/Screenshot_2022-06-17-23-52-39-97.jpg)

![](https://cdn.discordapp.com/attachments/979918594982936646/987384398083145778/Screenshot_2022-06-17-23-53-00-19.jpg)

After Installation, Run these following commands in Termux **One by One**. At anytime, termux will ask for confirmation so allow those requests.

This whole process will take 3-5 minutes so be patient.

```bash
add-apt-repository ppa:openjdk-r/ppa

apt-get install openjdk-17-jre
```
![](https://cdn.discordapp.com/attachments/979918594982936646/987385314538573844/Screenshot_2022-06-17-23-55-21-89.jpg)

![](https://cdn.discordapp.com/attachments/979918594982936646/987385314773438484/Screenshot_2022-06-17-23-55-53-79.jpg)

### Install Minecraft Server in your device

Open the Minecraft Server page by clicking this [link](https://www.minecraft.net/en-us/download/server)

In this page, tap and hold on `minecraft_server.1.19.jar` and copy the link

![](https://cdn.discordapp.com/attachments/979918594982936646/987386744511017020/Screenshot_2022-06-18-00-02-02-20.jpg)

![](https://cdn.discordapp.com/attachments/979918594982936646/987387307571183676/IMG_20220618_000429.jpg)


Now, go back to Termux and paste this command + the link you copied

```bash
wget -O server.jar
```
Example:
![](https://cdn.discordapp.com/attachments/979918594982936646/987388121547161650/Screenshot_2022-06-18-00-07-29-54.jpg)

After the download is complete, Paste this command.
```bash
chmod +x server.jar
```

Now. Run these following commands. It will let you access the EULA Agreement and will allow you to start your server and modify anything
```bash
apt-get install nano

nano eula.txt
```
You'll get prompted to a screen like this:

![](https://cdn.discordapp.com/attachments/979918594982936646/987389846282719302/Screenshot_2022-06-18-00-14-37-50.jpg)

Write this down to complete it:

![](https://cdn.discordapp.com/attachments/979918594982936646/987390285703176202/Screenshot_2022-06-18-00-16-14-89.jpg)

After that, Press **CTRL** and then **X**. It will ask for if you want to modify it, just press **Y** then **ENTER** to save it.

### Finally
Now you can start your server by runnning this command:
```bash
java -Xmx1024M -Xms1024M -jar server.jar nogui
```
## Socials

- [Github](https://github.com/AvinchYoshinova)
- [Discord Server](https://dsc.gg/lifelessmc)


## FAQ

#### How can I allocate more memory?

Answer: If you want to use more memory, simply multiply 1024 by 2 if you want 2GB, or 3 if you want 3GB. And edit startup command like this:

Example:
```bash
java -Xmx1024M -Xms3072M -jar server.jar nogui
```
But using much ram your device cannot handle might crash your server. For safer procedure, divide your available RAM by 2 and use that instead :)

#### How can I install plugins?
Answer: Join our discord server and I'll teach you how.
https://discord.gg/FRsej36qTb
