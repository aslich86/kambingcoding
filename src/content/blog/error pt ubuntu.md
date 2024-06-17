---
title: 'Install Packet Tracer di Ubuntu 23.10 ke Atas'
description: 'Anda menemukan Error di Ubuntu 23.10'
pubDate: 'Jul 15 2024'
heroImage: ''
---

###### If Cisco Packet Tracer installation on Ubuntu 23.10 gives you this error

```
    This package is uninstallable
    Dependency is not satisfiable: libgl1-mesa-glx
```
 link for  [guide](https://github.com/PetrusNoleto/Error-in-install-cisco-packet-tracer-in-ubuntu-23.10-Dependency-is-not-satisfiable-libgl1-mesa-glx)


###### If your Cisco Packet Tracer installation shows this error
 ```
  The following packages have unmet dependencies:
  packettracer: depends: libgl1-mesa-glx but it is not installable
```
  




##### Step 1 Download dependecies archives
  click [here](https://github.com/PetrusNoleto/error-in-install-cisco-packet-tracer-in-ubuntu-23.10---guide-instalation/releases/tag/CiscoPacketTracerFixUnmetDependenciesUbuntu23.10) for download dependecies


##### Step 2 install gdebi

```
  sudo apt install gdebi
```
##### Step 3 install dependecies
  go to the Downloads page
  
  in terminal
  ```
  cd /home/yourUser/Downloads
  ```
  install dependencies
  ```
    sudo gdebi ./libegl1-mesa_23.0.4-0ubuntu1.22.04.1_amd64.deb ./libgl1-mesa-glx_23.0.4-0ubuntu1.22.04.1_amd64.deb
  ```
##### Step 4 install CiscoPacketTracer
  ```
    sudo gdebi ./Packet_Tracer821_amd64_signed.deb 
  ```
  
  or
  
  ```
    sudo gdebi ./YOURPACKETTRACKERARCHIVE.deb 
  ```
