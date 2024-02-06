installation steps for ground station

# Hardware

ground station: Raspberry pi 5
wifi card : archer-t2u-plus (Realtek rtl8812au)

# OS 

Ubuntu

# install rtl8812au driver 

follow the instruction here https://github.com/svpcom/rtl8812au


```
$ git clone -b v5.2.20 https://github.com/svpcom/rtl8812au.git
$ cd rtl*
$ sudo apt-get install dkms
$ sudo apt-get install linux-headers-`uname -r`
$ sudo ./dkms-install.sh
```

# install qground control 
since qground control prebuilt binary only supports x86, we need to build it from source for raspberry pi arm64

install qt5 

sudo apt install qtbase6-dev qt5-qmake


https://docs.qgroundcontrol.com/master/en/qgc-dev-guide/getting_started/index.html

git clone --recursive -j8 https://github.com/mavlink/qgroundcontrol.git
git submodule update --recursive


# Install wfb-ng
https://github.com/svpcom/wfb-ng/wiki/Install-from-scratch