# Opi_Zero_3_power_opt
Various tweaks to reduce power consumption of the OrangePi Zero 3.  
You may disable unused peripherals like codec, gpu, hdmi ( with sound ).  
Kernel used is 5.4.125. Image is debian server.  

Compile with:  
<code> dtc -I dts -O dtb sun50i-h616-nogpu.dts > sun50i-h616-nogpu.dtbo </code>  

Copy to /boot/dtb/sunxi/overlay .  
Add <code> overlay=nogpu </code> to /boot/orangepiEnv.txt

You can lower ethernet speed with:  
<code> wmii-tool -F 100baseTx-FD eth0 </code>  

Ethtool is not working fot this specific kernel.
Check temp with:  
<code> cat /sys/class/thermal/thermal_zone?/temp </code> .  



