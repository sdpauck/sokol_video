# USBCamera
Use opencv to read the usb Camera

# requirement
opencv 3.4.3
GNU 5.4.0
cmake 3.12.0

```shell 
sudo apt-get install libopencv-dev
```

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

# Install OpenCV
Here's my short answer - maybe it will help: 
```
sudo apt-get install libopencv-dev python-opencv
```

From a fresh Raspbian I usually do/install the following first, as my work seems to depend on some of these libraries, so here's the full process I use to get OpenCV going:
```
sudo apt-get update; sudo apt-get upgrade

sudo apt-get -y install build-essential cmake cmake-curses-gui pkg-config libpng12-0 libpng12-dev libpng++-dev libpng3 libpnglite-dev zlib1g-dbg zlib1g zlib1g-dev pngtools libtiff4-dev libtiff4 libtiffxx0c2 libtiff-tools libeigen3-dev

sudo apt-get -y install libjpeg8 libjpeg8-dev libjpeg8-dbg libjpeg-progs ffmpeg libavcodec-dev libavcodec53 libavformat53 libavformat-dev libgstreamer0.10-0-dbg libgstreamer0.10-0 libgstreamer0.10-dev libxine1-ffmpeg libxine-dev libxine1-bin libunicap2 libunicap2-dev swig libv4l-0 libv4l-dev python-numpy libpython2.6 python-dev python2.6-dev libgtk2.0-dev

sudo apt-get install libgstreamer-plugins-base1.0-dev
```
Then finally 
```
sudo apt-get install libopencv-dev python-opencv
```