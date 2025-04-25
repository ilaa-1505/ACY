capstone@capstone-desktop:~/Downloads/rtl8188eu$ make
make: Warning: File 'Makefile' has modification time 17285 s in the future
make ARCH=arm64 CROSS_COMPILE= -C /lib/modules/4.9.201-tegra/build M=/home/capstone/Downloads/rtl8188eu  modules
make[1]: Entering directory '/usr/src/linux-headers-4.9.201-tegra-ubuntu18.04_aarch64/kernel-4.9'
rm: cannot remove '/home/capstone/Downloads/rtl8188eu/.tmp_versions/8188eu.mod': Permission denied
Makefile:1633: recipe for target 'crmodverdir' failed
make[1]: *** [crmodverdir] Error 1
make[1]: Leaving directory '/usr/src/linux-headers-4.9.201-tegra-ubuntu18.04_aarch64/kernel-4.9'
Makefile:155: recipe for target 'modules' failed
make: *** [modules] Error 2
capstone@capstone-desktop:~/Downloads/rtl8188eu$ make clean
make: Warning: File 'Makefile' has modification time 17272 s in the future
rm -fr *.mod.c *.mod *.o .*.cmd *.ko *~
rm -fr .tmp_versions
rm: cannot remove '.tmp_versions/8188eu.mod': Permission denied
Makefile:187: recipe for target 'clean' failed
make: *** [clean] Error 1
capstone@capstone-desktop:~/Downloads/rtl8188eu$ sudo make clean
[sudo] password for capstone: 
make: Warning: File 'Makefile' has modification time 17257 s in the future
rm -fr *.mod.c *.mod *.o .*.cmd *.ko *~
rm -fr .tmp_versions
rm -fr Module.symvers ; rm -fr Module.markers ; rm -fr modules.order
cd core ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
cd hal ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
cd os_dep ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
make: warning:  Clock skew detected.  Your build may be incomplete.
capstone@capstone-desktop:~/Downloads/rtl8188eu$ 





sudo rm -rf /home/capstone/Downloads/rtl8188eu/.tmp_versions
sudo rm -rf /home/capstone/Downloads/rtl8188eu/*.ko /home/capstone/Downloads/rtl8188eu/*.o /home/capstone/Downloads/rtl8188eu/*.mod.c
sudo rm -f /home/capstone/Downloads/rtl8188eu/Module.symvers


find /home/capstone/Downloads/rtl8188eu -exec stat {} \;


https://github.com/lwfinger/rtl8188eu





capstone@capstone-desktop:~/rtl8188eu$ make install
install -p -m 644 8188eu.ko  /lib/modules/4.9.201-tegra/kernel/drivers/staging/r8188eu/
install: cannot remove '/lib/modules/4.9.201-tegra/kernel/drivers/staging/r8188eu/8188eu.ko': Permission denied
Makefile:161: recipe for target 'install' failed
make: *** [install] Error 1





capstone@capstone-desktop:~$ sudo iw dev wlan0 info
command failed: No such device (-19)
capstone@capstone-desktop:~$ ifconfig
eth0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        inet 10.127.7.145  netmask 255.255.0.0  broadcast 10.127.255.255
        ether 48:b0:2d:2e:a5:98  txqueuelen 1000  (Ethernet)
        RX packets 6037  bytes 6327728 (6.3 MB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 55  bytes 5173 (5.1 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
        device interrupt 149  base 0xd000  

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 4005  bytes 326071 (326.0 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 4005  bytes 326071 (326.0 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

rndis0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        ether 22:87:03:80:82:2d  txqueuelen 1000  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 0  bytes 0 (0.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

usb0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        ether 22:87:03:80:82:2f  txqueuelen 1000  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 0  bytes 0 (0.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

wlan0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.137.210  netmask 255.255.255.0  broadcast 192.168.137.255
        inet6 fe80::1723:2709:c7e0:f0ee  prefixlen 64  scopeid 0x20<link>
        ether 3c:64:cf:d3:b0:b8  txqueuelen 1000  (Ethernet)
        RX packets 494  bytes 99112 (99.1 KB)
        RX errors 0  dropped 14  overruns 0  frame 0
        TX packets 291  bytes 38533 (38.5 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0



