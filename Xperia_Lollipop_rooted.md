#WIP
##all correclty so far, but needs typo fixes, pretty print and cleanup

Dear future myself,

here I tell you how to creat a pre-rooted firmware update for Sony Xperia (Z1 compact)

Prerquities:
- Xperia (Z1 compact) device stock(?) KitKat rooted (Newroot worked just fine without unlocking the boot loader: )
- some custom recovery, the fancy dual recovery works just fine
 install from rooted kitkat (dual recovery from http://nut.xperia-files.com/)

Tools needed:
- FlashTool: http://www.flashtool.net/index.php
- XPeriFirm: http://forum.xda-developers.com/crossdevice-dev/sony/pc-xperifirm-xperia-firmware-downloader-t2834142
ahh no longer needed, as it's integrated in FlashTool now
- PRFCreator: http://forum.xda-developers.com/crossdevice-dev/sony/tool-prfcreator-easily-create-pre-t2859904


Part 1: get a ftf file of the disred firware
See also: http://www.xperiablog.net/2014/08/16/create-your-own-ftf-firmware-files-using-xperifirm-and-flashtool-guide/
Download  Firmware with XperiFirm with auto-unpack
Use FlashTool Bundle-Create
	Select Unacked firware path
	Select Device From list
	Add branding info: Vodafone DE
	add Firware versiion: 
	add all but the .ta files to the right listview
	DELETE the fwinfo.xml in unpacked fw folder
	create
	done. ftf file is in configured user home: C:\Users\USERNAME\.flashTool
	
Part 2: get your ftf fike pre-rooted
1. Download latest SuperSU: https://download.chainfire.eu
2. Open PRFCreator
3. add D5503_14.5.A.0.270_Vodafone DE.ftf as ftf file
4. add UPDATE-SuperSU-v2.46.zip as supersu zip
5. not needed, but also not wrong: add Z1C-lockeddualrecovery2.8.15-RELEASE.flashable.zip as recovery (dual recovery from http://nut.xperia-files.com/)
6. check all checkboxes, but rhe "sign zip"
7. mybe add extra zip
8. create
9. done. find flashabe.zip in PRFCreator folder (got to propose the outfilename= FTF-file_pre-rooted_flashable.zip format)

Part 3: flash your zip
1. have 3 coffees
2. nandroid backup your phone
3. get really nervous
4. wipe dalvik and cache to get a better feeling
4. try dirty flash the new firware (OTA is also applied dirty, isn't it?)
5. whoa, flashing was fast
4. wipe dalvik and cache again could help prevent the unpredicted... could it?
6. AAAAHHH! booting takes so looong
7. Yeah! 386 Apps getting optimized...
8. looks good
9. hu? NFC firware update? OK go on
10. Update for Google play services? go on
11. done.

Part 4: Xposed
Now go on and install Xposed Framework 3.0 beta 4 and hope for the best :D
1. eh - bootlooop :/
2. done
