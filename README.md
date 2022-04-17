# HP-OMEN-15-ce0xx-Monterey-OC
****SPECS****
<li>
  <ul>CPU- I5-73000HQ</ul>
  <ul>IGPU- INTEL HD 630</ul>
  <ul>DGPU- GTX 1050TI Disabled</ul>
  <ul>Audio- ALC295 (Layout-id=3)</ul>
  <ul>Wifi and Bluetooth- Intel Dual Band AC</ul>
</li>

***THINGS TO REMEMBER****
1. Flash your own SMBIOS from SMBIOSGen
2. Reset NVRAM for sure
3. Charge once full to 100% and drain the battery fully it will calibrate and improve battery life.
4.  Unlock CFG lock specifying steps below ** It is mandatory because it will unlock cpu configuration by patches.

That's all

*****GUIDE FOR UNLOCKING CFG LOCK****
1. Download Latest Bios firmware ( it will be downloaded in exe format so run it once and it will extract the files in C drive *Run on Windows*)
2. Download Ifrextract from here- https://github.com/donovan6000/Universal-IFR-Extractor.git
3. Download UEFITool from here- https://github.com/LongSoft/UEFITool.git
4. Extract the Setup.bin PE32 Image Section (the one UEFITool found) through Extract Body menu option.
5. Run IFR-Extractor on the extracted file (e.g. ./ifrextract Setup.bin Setup.txt).
6. Find CFG Lock, VarStoreInfo (VarOffset/VarName): in Setup.txt and remember the offset right after it (e.g. 0x123).
7. Download and run Modified GRUB Shell compiled by brainsucker or use a newer version by datasone.
8. Enter setup_var 0x123 0x00 command, where 0x123 should be replaced by your actual offset, and reboot.

Here we go fully stable and everything works no need to work on anything just copy,


IF YOU GET ANY BUGS OR ISSUES PLEASE PULL A REQUEST WILL IMPROVE OR FIX THAT.

Thanks.
