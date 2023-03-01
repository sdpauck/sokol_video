# USBCamera
Use opencv to read the usb Camera

# requirement
opencv 3.4.3
GNU 5.4.0
cmake 3.12.0

# Run
```shell 
mkdir build && cd build
cmake ..
make -j7

```

# Notice
capture.open("/dev/video0") need to use your own camera device path.

# see usb 
`lsusb`

# See usb camera device
```shell
ls | grep /dev/video

#see video0 detail info
udevadm info --query=all --name=/dev/video0
```

