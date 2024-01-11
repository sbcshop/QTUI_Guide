### QT for Linux/X11 (mostly focus Ubuntu 22.04.3 LTS) instructions

Commands to get essential C++ tools first before QT creator download and installation,
```
$ sudo apt update
$ sudo apt-get install build-essential libgl1-mesa-dev
```
verify with below commands,
```
$g++ --version
$make --version
```
After this head to download online installer for open source version :
[Download QT Community Edition](https://www.qt.io/download-qt-installer-oss?hsCtaTracking=99d9dd4f-5681-48d2-b096-470725510d34%7C074ddad0-fdef-4e53-8aa8-5e8a876d6ab4) 

We need to make downloaded file as executable. Also, will libxcb-xinerama0 for installer to run
Setup Commands Used:
```
$ chmod +x qt-unified-linux-x64-4.6.1-online.run
$ sudo apt install --reinstall libxcb-xinerama0 
$ ./qt-unified-linux-x64-4.6.1-online.run
```

Once you are done installing QT, you might face issue loading QT creator.
<img src="https://media.discordapp.net/attachments/1193090729845723168/1193101468031533139/10wPE.png?ex=65ab7d54&is=65990854&hm=bf88879267651d2c9b5db186da14ee382d7dbb28542918c78af80d621971d4ec&=&format=webp&quality=lossless&width=1245&height=210">

So, to solve above issue you need to install libxcb-cursor0 which helps in loading QTcreator
```
$ sudo apt-get install libxcb-cursor0
```

Sometimes you will get apt-get install issue, unable to connect or download package. 
If facing such issue with apt-get install package, make sure to select options listed in Software & Updates of Ubuntu.
<img src="https://media.discordapp.net/attachments/1193090729845723168/1194679639105343518/software_update_setting.png?ex=65b13b1e&is=659ec61e&hm=9ceb7fb3e6fdfdcad8216bc73f778dd3e956b578875afe9be42debe44468c30e&=&format=webp&quality=lossless&width=1180&height=563">

Once done restart terminal and try apt install any packages.
