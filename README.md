fork of [this](https://github.com/khuedoan/slock)

slock scren locker with blur and time for xorg

## Requirements

In order to build slock you need the Xlib header files.

## Installation

```sh
make
```
```sh
sudo make install
```
## Running slock

Simply invoke the 'slock' command. To get out of it, enter your password.

## Blur effect

This fork leverages picom's new kawase blur method instead of taking a screenshot, blur it using ImageMagick without hardware acceleration and then set it as the lock screen wallpaper.
The end result is much higher performance and much lower latency.

in picom config add 
```
opacity-rule = [ "80:name = 'slock'"] 
```
and 
```
blur:
{
    method = "dual_kawase";
    strenght = 5;
}
```
