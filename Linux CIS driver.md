# Linux CIS driver

- GPIO
    - https://moon-half.info/p/4570

- makefile
```=makefile  
PWD := $(shell pwd)
KERNEL=/lib/modules/`uname -r`/build
 
obj-m := vgpio.o
 
SRC=gpiochip.o
vgpio-objs = $(SRC)
 
 
all:
        $(MAKE) -C $(KERNEL) M=$(PWD) modules
 
clean:
        $(MAKE) -C $(KERNEL) M=$(PWD) clean
```
--- 

- uname:https://www.cnblogs.com/douJiangYouTiao888/p/6474035.html　系統有關訊息

- obj-m: 把.o當成module編譯 不會編進kernel

- v4l2:https://www.twblogs.net/a/5b825df82b717766a1e7f024
    - ctrls: https://01.org/linuxgraphics/gfx-docs/drm/media/kapi/v4l2-controls.html