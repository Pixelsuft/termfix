# Running On Android

## Requirements
 - [Termux](https://play.google.com/store/apps/details?id=com.termux)
 - [VNC Viewer](https://play.google.com/store/apps/details?id=com.realvnc.viewer.android)
 - File Storage Access for Termux (in Settings)

## Termux

Default Commands:
```sh
apt update
apt upgrade -y
apt update
pkg install x11-repo -y
apt update
exit
```

Restart Termux, then:
```sh
apt install -y sdl sdl2 tigervnc wget
```

Downloading Termfix:
```sh
wget https://github.com/Pixelsuft/termfix/releases/download/v1.0/termfix
chmod +x ./termfix
```

Running:
```sh
vncserver :1 -geometry -geometry- # Where -geometry- - Guest OS Resolution, for example: 640x480
export DISPLAY=":1"
./termfix -c -path-to-config- # Where -path-to-config- - Path To Config, for example: /storage/emulated/0/termfix/winxp.conf
```

Open VNC Viwever and connect to `localhost:1` <br /> <br />

When you want to Exit:
```sh
# Press Ctrl + C to quit from TermFix
vncserver -kill :1
exit
```
