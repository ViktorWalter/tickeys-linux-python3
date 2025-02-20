Bug or question?

Please tell me in issue.

[![Join the chat at https://gitter.im/BillBillBillBill/Tickeys-linux](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/BillBillBillBill/Tickeys-linux?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
![Tickeys Icon](http://img.blog.csdn.net/20150802103616846)

# Introduce
Tickeys is an powerful keyboard sound effect tool。Tickeys now brings seven sound styles，include Bubble, Typewriter, Mechanical, Sword, etc.

This tool have Windows and Mac version，Mac Version:([GitHub](https://github.com/yingDev/Tickeys))

# Project Website
http://www.yingdev.com/projects/tickeys

#　PyPI
https://pypi.python.org/pypi/tickeys

# Tickeys Mac Version
https://github.com/yingDev/Tickeys

# Install
Tickeys has not been fully tested to install in different distribution yet, some distribution may need installing related requirements.

## Compile(Build from source, need requirements)：

### Ubuntu:
1. To compile:
```
git clone git@github.com:ViktorWalter/tickeys-linux-python3.git
cd tickeys-linux-python3
./dependencies.sh
./build.sh #or build32.sh

```
2a. To run directly:

```
./run.sh
```
2b.
  1. To build a .deb package

```
./deb.sh #or deb32.sh
```

  2. To install from the package and run

```
sudo dpkg -i ./dist/tickeys_*.deb
```


#### Quick Compile Install：

* execute `sudo apt-get install python-dev python-pip python-kivy xdotool && sudo easy_install tickeys`。
* execute `sudo easy_install tickeys` or `sudo pip install tickeys`
* Use command `sudo tickeys` to open (`sudo tickeys -c` for CLI version)


#### Running Problem

* Couldn't hide window：

Solve：execute `sudo apt-get install xdotool ` to install xdotool

* no setuptools or pip

Solve：execute `sudo apt-get install python-pip` to install

* Python.h：no such file

Solve：execute `sudo apt-get install python-dev` to install

* ImportError: No module named Cython.Distutils

Solve：execute `sudo easy_install cython` to install

* ImportError: libSDL-1.2.so.0: cannot open shared object file: No such file or directory

    Solve：execute `yum install libSDL-1.2.so.0` to install

* NotImplementedError: mixer module not available

    Solve：same with above

Debian and Ubuntu User may try to install:

    * sudo apt-get install xdotool
    * sudo apt-get install libsdl1.2-dev
    * sudo apt-get install libsdl-mixer1.2
    * sudo apt-get install libsdl-ttf2.0

# How to use
Root permission is needed，implement the CLI and GUI version，GUI version is run by default，it will auto hide after open，press QAZ123 to show the window of tickeys.


# How to Develop
* ####Code Style: PEP8

* ####Application UI framework：Kivy

* ####Open sources license： MIT License

Install requirements：

    pip install -r requirements.txt

# Project struct
Tickeys-linux
```
├── AUTHOURS
├── build.sh
├── build.spec               pyinstaller
├── Changelog
├── deb.sh
├── dist
│   ├── make_deb.sh          script for deb
├── lib                      lib for run
├── LICENSE
├── MANIFEST.in
├── README.md
├── screenshot
├── setup.py
├── tickeys
│   ├── locale              translation
│   ├── build.py            cx_freeze(desperate)
│   ├── CLI.py              start CLI
│   ├── config.py           config controller
│   ├── GUI.py              start GUI
│   ├── __init__.py
│   ├── keyboardHandler.py  handler keyboard events
│   ├── logger.py
│   ├── requirements.txt
│   ├── Resources
│   │   ├── data
│   │   │   ├── bubble
│   │   │   ├── Cherry_G80_3000
│   │   │   ├── Cherry_G80_3494
│   │   │   ├── drum
│   │   │   ├── mechanical
│   │   │   ├── sword
│   │   │   └── typewriter
│   │   │   ├── schemes.json
│   │   └── fonts
│   │       └── DroidSansFallbackFull.ttf
│   ├── run.py            entry
│   ├── run_with_CLI.py   entry with CLI
│   ├── soundPlayer.py
│   ├── startupHandler.py
│   ├── tickeys
│   ├── tickeys.png
│   ├── tickeys_tray.py   (not use)
│   ├── tickeysui.kv      (desperate)
│   └── windowManager.py
└── tickeys.egg-info
```

# Author
Huang Xiongbiao

billo@qq.com
