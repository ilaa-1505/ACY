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
