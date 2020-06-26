# UX305FA - Catalina Guide



## CLOVER
### macOS version 10.15.0 to 10.15.3
 Use the Clover version, otherwise you will never be able to boot as EC map definition changed in newer macOS releases. 
 
 ## OPENCORE
 ### macOS version 10.15.4 to 10.15.6
 Use the OpenCore version. It's easier, faster, more intuitive and it's the only working bootloader for the UX305 for macOS 10.15.13+.
 	
    known bug : Bootcamps does not work, OC has a ACPI issues that inject patched definition while booting other OS which lead to Blue Screens and crashes. 
	To dual boot, install as normal with Bootcamps but you need to boot from BIOS the Windows partition instead of using OC EFI bootloader. 
    

### Requirement : 

- SSDT/DSDT from this git repo

- Clover EFI Bootloader (rev. 5102)/ OpenCore (latest release)

- UEFI drivers (Clover version and OC version) 

- Asus FN Key Kext included in both versions

  



Here's a quick table of what is working and what is not. 

|       Device        |          ID/SPECS          |  Working status   |
| :-----------------: | :------------------------: | :---------------: |
|         GPU         | INTEL HD 5300 1500MB VRAM  |      WORKING      |
|         CPU         |     CORE M 5Y10C 2C/4T     |      WORKING      |
|        WIFI         |   INTEL WIRELESS-AC7265    |  WILL NEVER WORK  |
|         USB         |        3.0 GENERIC         |      WORKING      |
| FUNCTION KEYS (FN)  |      FN + {F1 TO F12}      | PARTIALLY WORKING** |
|     BRIGHTNESS      |             -              |      WORKING      |
|      TRACKPAD       |  ASUS/APPLE MULTIGESTURE   |      WORKING      |
|   COMMAND BUTTON    |             -              |      WORKING      |
|      BLUETOOTH      |             -              | PARTIALLY WORKING |
|  IMESSAGE/FACETIME  |             -              |    NOT WORKING    |
|      APP STORE      | CONNECTION/INSTALLING APPS | 	  WORKING 	   |
| SLEEP/WAKE FROM LID |             -              |      WORKING      |
|       WEBCAM        |       POTATO QUALITY       |      WORKING      |

** all functions works, however for brightness you only need to setup a shortcut in the settings with the F3 and F4 keys. 