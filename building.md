# Building for Android

## Requirements
 - [Termux](https://play.google.com/store/apps/details?id=com.termux)
 - [VNC Viewer](https://play.google.com/store/apps/details?id=com.realvnc.viewer.android)
 - File Storage Access for Termux (in Settings)

## Termux

Default Commands:
```sh
apt update -y
apt upgrade -y
pkg install x11-repo -y
apt update -y
exit
```

Restart Termux, then:
```sh
apt install -y nodejs clang sdl sdl2
```

Download TermFix source, unzip it, then:
```sh
cd -path-to-termfix- # Where -path-to-termfix- - Path To TermFix, for example: /storage/emulated/0/termfix
node makefile --cc clang release
```

Now we got builded `termfix` file
