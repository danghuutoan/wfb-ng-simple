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
$ apt-get install linux-headers-`uname -r`
```