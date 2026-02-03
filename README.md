## What it is
A basic devcontainer to use the pico C-SDK
(and hopefully the simplest )
## Features
- C compiler stuff (gcc, cmake, ...)
- microcom (serial monitor)

## usage
check if you have access to the pico on host
```code
ls -l /dev/ttyACM*
```

then make sure you are in the ```dialog group``` on host
```code
groups
```
and if you are not, put yourself in it 
```code
sudo usermod -aG dialout $USER
```
and reload the sesion
or follow this post if you are on atomic:
[fedora Discussion](https://discussion.fedoraproject.org/t/how-to-add-myself-to-the-dialout-group/24147/2)

then clone this repo
```code
https://github.com/LostFlashlight/pico-sdk-devcon.git
```
to run the devcontainer i would recomend **DevPod** combined with **VScodium**(native)
```code
flatpak install flathub sh.loft.devpod
```
https://github.com/VSCodium/vscodium/releases
