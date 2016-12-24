MCPE Raspberry Pi Launcher
===================

## Required packages

```
    sudo apt-get install zlib1g-dev libncurses5-dev libgles2-mesa-dev zlib1g-dev libx11-dev linux-libc-dev uuid-dev libpng-dev libxext6
```

You will also need to build cmake from source for armv7 Linux. You can get the cmake Linux source from [here](https://cmake.org/files/v3.7/cmake-3.7.1.tar.gz), and build directly on the Raspberry Pi:

```
	./bootstrap
	sudo make package install
```

This will take over an hour on the Pi, so be patient.


## Compiling
This app uses cmake so it is enough to do:

```
    cmake .
    make
```

## Running
1. Clone this repository
2. Compile the launcher (see above)
3. You'll need to obtain an MCPE .apk. The easiest way to do so is to use @MCMrARM's
[Google Play downloader tool](https://github.com/MCMrARM/google_play_downloader) (You need Java to run. It is an console app; type 'n' when asked if you want to download the x86 version of the app (raspberry pi is ARM). You must have purchased MCPE
on the Google account you are logging in with; the package name of MCPE is `com.mojang.minecraftpe`)
4. After you have downloaded MCPE, place it in the directory where you'll be running this app, and run ./extract.sh _filename_
5. Run the launcher!


## License and thanks
This Project is a fork of @MCMrARM's [Linux MCPE Launcher](https://github.com/MCMrARM/mcpelauncher-linux). All ARMv7 and Raspberry Pi changes are made by me.
Most of the code in this repo is licensed under BSD. This project uses libc, libstdc++, libz and libm - libraries
extracted from the Android OS. A modified version of libhybris is also included, which is licensed under GPL. This project
also uses the EGLUT library and FMOD library (for sound).
