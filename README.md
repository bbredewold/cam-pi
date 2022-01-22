# Cam-PI

Cam-PI is a nice interface for connecting a DroidCam stream to an HDMI input.

## Setup

- Raspberry Pi OS (32bit) Lite (Debian BullsEye) on Raspberry PI 3
- Install VLC
- Replace "dtoverlay=vc4-kms-v3d" with "dtoverlay=vc4-kms-v3d-pi4" in the /boot/config.txt.
- cvlc --network-caching=0 http://192.168.88.179:4747/video?1280x720 vlc://quit
- For connecting to Atem: 50Hz needed when setting the hdmi_mode. (https://elinux.org/RPiconfig#Video_mode_options)

```
curl -fsSL https://deb.nodesource.com/setup_17.x | sudo -E bash -
sudo apt-get install -y nodejs
```

Inspiration got from https://github.com/Anonymousdog/displaycameras/ but omxplayer is depricated, therefore VLC is used
