### 1. NVIDIA-SMI has failed because it couldn't communicate with the NVIDIA driver (Software & Update).
#### Problems
- This issue happens when your computer can not detect or communicate with Nvidia driver.
- This could lead to that we can not use our GPU even having.
#### Reasons
- In installation phase, maybe Nvidia driver was disabled.
- Our ubuntu version is not compatible with current Nvidia driver.
#### Solutions
1_1. Access <strong> Software & Update </strong>, choose <strong> Additional Drivers </strong>. Then choose <strong>NVIDIA Driver Metapackage ... (priorietary)</strong>. Then enter <strong> Configrating Boot Password </strong>, reboot.   
1_2. In boot menu, choose <strong> Enroll MOK </strong>, type the key already created when installing Nvidia driver, continue.   
/   
2. In case the 1st Solution can not solve the problem. Try the way mentioned in the link below.   
https://askubuntu.com/questions/927199/nvidia-smi-has-failed-because-it-couldnt-communicate-with-the-nvidia-driver-ma  
/   
Sometimes, up to the devices, they might <strong>NOT</strong> require Configurating Boot Password. Just need to restart the device, then changes will be applied.
#### Check result
```
nvidia-smi
```
After entering this command, if "NVIDIA-SMI has failed because it couldn't communicate with the NVIDIA driver" does not appear or display as the picture below, it's okay.   
![alt text](images/nvidia-smi.png "nvidia-smi")
- Tested devices: ASUS TUF GAMING A17(AMD Ryzen), LEGION 5(AMD Ryzen), MSI(Intel)

### 2. Install Nvidia Driver with command lines
If you don't want to install with <strong>Software and Update</strong> app, you could use command line to install Nvidia Driver.
- Firstly, check the drivers that suit your OS or recommended drivers you should use. Your terminal response may vary with image below
```
ubuntu-drivers devices
```
![alt text](images/nvidia-drivers.png "nvidia-drivers")   
- Assume you want to install <strong>nvidia-driver-535</strong>, use the below commands.
```
sudo apt install nvidia-driver-535
sudo reboot
```
#### Check result 
```
nvidia-smi
```


