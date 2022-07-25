# Luxonis 

## TODO

ask [stackoverflow](https://stackoverflow.com/questions/ask)

## Tips

:::info
[Hackmd新功能](https://hackmd.io/@hackmd/2019-in-review), include vscode extension
:::

擴充WSL VHD容量,see [this doc](https://docs.microsoft.com/zh-tw/windows/wsl/vhd-size)

pretify wsl2, see [this](https://dev.to/rishabk7/beautify-your-terminal-wsl2-5fe2) instruction

NATed bridge, see [this](https://www.tecmint.com/create-network-bridge-in-ubuntu/)

### Virsh Issue

:::danger
```bash=
kai@DESKTOP-8DBT08O:/mnt/c/Users/GUO/Desktop/Ting-Kai_Kuo_Projects$ sudo virsh --connect=qemu://system net-autostart default
error: failed to connect to the hypervisor
error: internal error: invalid URI qemu://system (maybe you want qemu:///system)
kai@DESKTOP-8DBT08O:/mnt/c/Users/GUO/Desktop/Ting-Kai_Kuo_Projects$ sudo virsh --connect=qemu:///system net-autostart de
fault
error: failed to connect to the hypervisor
error: Failed to connect socket to '/var/run/libvirt/libvirt-sock': No such file or directory
```

refer to [this solution](https://wiki.libvirt.org/page/Failed_to_connect_to_the_hypervisor)
    - [hypervisor wiki](https://zh.wikipedia.org/zh-tw/Hypervisor)
:::

:::info
- run RP-Pi os with Qemu tutorial 2, see [this](https://linuxconfig.org/how-to-run-the-raspberry-pi-os-in-a-virtual-machine-with-qemu-and-kvm)
    - device tree, see [this](https://ithelp.ithome.com.tw/articles/10242811)
        - [MMIO](https://www.itsfun.com.tw/MMIO/wiki-603031-963321)
            - review [PCI](https://tw.coderbridge.com/series/c52316e2d64e49049c6f8fc151d89466/posts/aee48de22d9a46e78fe676821d75c482)
                - [pciutils](https://github.com/pciutils/pciutils)

:::

:::danger
```bash=
kai@DESKTOP-8DBT08O:/mnt/c/Windows/System32$  sudo systemctl start libvirtd
System has not been booted with systemd as init system (PID 1). Can't operate.
Failed to connect to bus: Host is down
```

[change *SYSTEMD* solution](https://ithelp.ithome.com.tw/articles/10255920)

:::

:::danger
```bash=
kai@DESKTOP-8DBT08O:/mnt/c/Windows/System32$ sudo git clone https://github.com/DamionGans/ubuntu-wsl2-systemd-script.git
fatal: could not create work tree dir 'ubuntu-wsl2-systemd-script': Permission denied
```

solution: 
```bash= 
sudo chmod o+w dirname
```

:::


:::danger
```bash=
kai@DESKTOP-8DBT08O:/mnt/c/Windows/System32$ sudo virt-install \
>   --name rpios  \
>   --arch armv6l \
>   --machine versatilepb \
>   --cpu arm1176 \
>   --vcpus 1 \
>   --memory 256 \
>   --import  \
>   --disk 2021-01-11-raspios-buster-armhf-lite.img,format=raw,bus=virtio \
>   --network bridge,source=virbr0,model=virtio  \
>   --video vga  \
>   --graphics spice \
>   --boot 'dtb=qemu-rpi-kernel/versatile-pb-buster.dtb,kernel=qemu-rpi-kernel/kernel-qemu-4.19.50-buster,kernel_args=root=/dev/vda2 panic=1' \
>   --events on_reboot=destroy
ERROR    Error: --disk 2021-01-11-raspios-buster-armhf-lite.img,format=raw,bus=virtio: Size must be specified for non existent volume '2021-01-11-raspios-buster-armhf-lite.img'
```
possible [solution](https://www.spinics.net/linux/fedora/libvirt-users/msg11740.html)

:::

## Compression

- [H.264/H.265](https://github.com/leandromoreira/digital_video_introduction/blob/master/README-cn.md#%E7%AC%AC%E5%85%AD%E6%AD%A5---%E6%AF%94%E7%89%B9%E6%B5%81%E6%A0%BC%E5%BC%8F)
    - [H264 wiki](https://zh.wikipedia.org/zh-tw/H.264/MPEG-4_AVC)
        - [ITU-T](https://zh.wikipedia.org/zh-tw/%E5%9C%8B%E9%9A%9B%E9%9B%BB%E4%BF%A1%E8%81%AF%E7%9B%9F%E9%9B%BB%E4%BF%A1%E6%A8%99%E6%BA%96%E5%8C%96%E9%83%A8%E9%96%80)
            - [ITU-T VCEG](https://zh.wikipedia.org/zh-tw/ITU-T_VCEG)
        - [IEC](https://zh.wikipedia.org/zh-tw/%E5%9B%BD%E9%99%85%E7%94%B5%E5%B7%A5%E5%A7%94%E5%91%98%E4%BC%9A)
        - [**Motion Compensation**](https://zh.wikipedia.org/zh-tw/%E8%BF%90%E5%8A%A8%E8%A1%A5%E5%81%BF)
        - [RTP(real time protocol)](https://zh.wikipedia.org/zh-tw/%E5%AE%9E%E6%97%B6%E4%BC%A0%E8%BE%93%E5%8D%8F%E8%AE%AE) 
- [DM1095_OAK-D-LITE-DEV_DepthAI_USB3C](https://github.com/luxonis/depthai-hardware/tree/master/DM1095_OAK-D-LITE-DEV_DepthAI_USB3C)

## DepthAI

> 2022 07 22 更新

以DepthAI(python api)為主要目標

- curl argument
```bahsh
-l, --list-only     List only mode
     --local-port <num/range> Force use of RANGE for local port numbers
     
-F, --form <name=content> Specify multipart MIME data
     --form-string <name=string> Specify multipart MIME data
     --ftp-account <data> Account data string
     --ftp-alternative-to-user <command> String to replace USER [name]
     --ftp-create-dirs Create the remote dirs if not present
     --ftp-method <method> Control CWD usage
     --ftp-pasv      Use PASV/EPSV instead of PORT
```

Review pipeline "|" 用法, see [this](https://www.hy-star.com.tw/tech/linux/pipe/pipe.html#50)
```bash=
stdout of command 1 | stdin of command 2
```

- CV and Embedded ML, see [this](https://github.com/ShawnHymel/computer-vision-with-embedded-machine-learning)



[Raspberry PI camera emulator](https://forums.raspberrypi.com/viewtopic.php?t=99547)，要[安裝](https://www.linux-projects.org/uv4l/installation/)在qemu Respberry PI ARM系統上面

[lepton(decompression tool)](https://github.com/dropbox/lepton)
    - [bandwidth compression](https://en.wikipedia.org/wiki/Bandwidth_compression)

## QEMU Issue

:::danger
```bash=
alsa: Could not initialize DAC
alsa: Failed to open `default':
alsa: Reason: No such file or directory
audio: Failed to create voice `lm4549.out'
gtk initialization failed
```

- ["could not initialize DAC" issue](https://github.com/google/syzkaller/issues/250)
    - review digital-analog converter
        - [MCP4728 DAC(python)](https://github.com/HydraSpex/MCP4728)
        - [rust DAC emulator](https://docs.rs/ether-dream-dac-emulator/latest/ether_dream_dac_emulator/)
:::


## Luxonis [Simulation](https://github.com/luxonis/simulation/tree/main/blender-data-augmentation-example)
- fspy [source](https://fspy.io/) and [repo](https://github.com/stuffmatic/fSpy-Blender)