# Lenovo-Legion-Y520-Osx

This guide os for below below model and OSX 10.13.5

 - Intel Core i5-7300HQ Processor ( 2.50GHz 2400MHz 6MB )
 - 8.0GB PC4-19200 DDR4 SODIMM 2400MHz 
 - NVIDIA GeForce GTX1050 4GB GDDR5(Disabled via DSDT/SSDT Patching)
 - Qualcomm Atheros QCA6174A 
 - Audio Realtek (ALC3248 as shown in windows 10)
 - Realtek Lan(Works out of the box)


# What doesnt work
- Inbuilt wifi
- sleep

# Wifi Dongle
I am using D-Link DWA-131 Wireless N Nano USB Adapter 

# Installation Guide



# Post Installation Guide
 (WIP)

Post install almost everything works,but audio via jack doesnt work, need to disable gfx to save power

- Open Clover and put the following configurations 
- Use these kexts(All up to date as of Jul 31st 2018). You can get latest kexts if provided kexts are older 
- Fix Audio and input jack(the above kext files in conjuction with Clover conifg will takecare of this)
- Disable 1050/ discrete graphics. https://www.tonymacx86.com/threads/guide-disabling-discrete-graphics-in-dual-gpu-laptops.163772/ .  In my case i had to patch only one SSDT-8.aml file .In Clover config put SSDT-PNLF.aml file last in load order. You can check screenshot in Clover ACPI section.
- Fix powermanagement-(already provided in clover config)
