# Hackintosh-Dell-7060-mff
Hackintosh macOS12 for Dell 7060 mff, based on Opencore v0.7.8  

对于安装macOS 12.4 Monterey的 请使用`EFI0.7.8_macOS12_WIFIfixed.zip`  

对于安装macOS 11.6 bigSur的 请使用`OC0.7.8.zip` 

## 硬件总览  
准系统: Dell OptiPlex 7060 mff  
CPU: Intel Core i5 8600T (6C6T)  
GPU: UHD630  
内存: 8GiB x 2 16G  
硬盘: WD SN550 1T  
无线网卡: BCM 94352Z/DW1560  

## 硬件运行情况  
### 正常  
WIFI，蓝牙，双向隔空投送，双向接力，热点，以太网口  
核心显卡 硬件解码，HIDPI  
3.5mm耳机接口  
完美睡眠  
### 不正常
DP，HDMI显示器音频  
12.4系统下隔空投送  

## BIOS设置 -> F2  
General → Advanced Boot Options: `uncheck`  
System Configuration → SATA Operation: `AHCI`  
Secure Boot → Secure Boot Enable: `Disabled`  
Intel® Software Guard Extensions™ → Intel® SGX™ Enable: `Disabled`  
Power Management → Block Sleep: `uncheck`  
Virtualization Support → VT for Direct I/O: `uncheck`  

## 开始之前 -> Grub中设置BIOS  
设置显存预分配到64M: `setup_var 0x8DC 0x02`  
关闭CFGlock: `setup_var 0x5BE 0x00`  

