|==================================|
| Program Name: | DVD Decrypter    |
|==================================|
| Author:       | LIGHTNING UK!    |
|==================================|

Supported Command Line Switches:

(You can get a basic version of this list via 'DVDDecrypter.exe /?')

/MODE <IFO | FILE | ISOREAD | ISOWRITE>
	Used to tell the program which 'Mode' to open up in.

/SRC <Drive Letter | SCSI Address> | "<File Name>"
	Used to select the source drive or filename.
	Drive Letter or SCSI Address applies to IFO, FILE and ISOREAD modes.
	File Name applies to ISOWRITE mode.
	Examples: /SRC J:
		  /SRC 1:0:0
		  /SRC "C:\DVDIMAGE.ISO"

/DEST "<Folder | File Name>" | <Drive Letter | SCSI Address> 
	Used to select the destination folder, filename or drive.
	Folder applies to IFO and File modes.
	File Name applies to ISOREAD mode.
	Drive Letter or SCSI Address applies to ISOWRITE mode.
	Examples: /DEST "C:\DVD 1\VIDEO_TS\"
		  /DEST "C:\DVDIMAGE.ISO"
		  /DEST J:
		  /DEST 1:0:0

	You can use [DISC_LABEL] within the path to have the program insert the disc's volume label.
	Examples: /DEST "C:\[DISC_LABEL]\VIDEO_TS\"
		  /DEST "C:\[DISC_LABEL].ISO"

/VTS <VTS Number>
	Used to tell the program which VTS should be selected by default.
	Applies to IFO mode only
        Required when /PGC is specified
	Example: /VTS 1

/PGC <PGC Number>
	Used to tell the program which PGC should be selected by default.
	Applies to IFO mode only
        Required when /VTS is specified
	Example: /PGC 1

/ANGLE <Angle Number>
	Used to tell the program which PGC should be selected by default.
	Applies to IFO mode only
	Example: /ANGLE 1

/DIRECT <Stream Number> <...>
	Used to tell the program which streams should be processed using the 'Direct Stream Copy' method.
	Applies to IFO and File modes.
	'*' and '?' wildcards can be used.
	Examples: /DIRECT 0x80 0xE0
		  /DIRECT 0x8? 0x?0
		  /DIRECT *

/DEMUX <Stream Number> <...>
	Used to tell the program which streams should be processed using the 'Demux' method.
	Applies to IFO and File modes.
	'*' and '?' wildcards can be used.
	Examples: /DEMUX 0x80 0xE0
		  /DEMUX 0x8? 0x?0
		  /DEMUX *

/RAW <Stream Number> <...>
	Used to tell the program which streams should be processed using the 'Raw' method.
	Applies to IFO and File modes.
	'*' and '?' wildcards can be used.
	Examples: /RAW 0x80 0xE0
		  /RAW 0x8? 0x?0
		  /RAW *

/START
	Used to start the decryption process automatically when the program has finished initialising.
	Basically, it just presses the 'Decrypt' / 'Write' button for you!

/CLOSE
	Used to close the program when the decryption process has finished.
	Basically, it just presses the 'Close' button for you!

/VERIFY <YES | NO>
	Used to make the program verify a disc is readable after it has been written in ISO Write mode.
	Basically, it just checks (or unchecks!) the 'Verify after write' box for you!

/SHUTDOWN
	Used to shutdown the computer when the program has finished burning in ISO Write mode.
	Basically, it just checks the 'Shutdown computer when done' box for you!

/OVERWRITE <YES | NO>
	Used to force the program to either overwrite all existing files, or never overwrite them.

/ERASE
	Used to automatically erase / format / overwrite media in ISO Write mode.

/SPEED <Write Speed>
	Used to change the value of the 'Write Speed' drop down list.
	The parameter must match the value within the drop down list exactly.
	Examples: /SPEED MAX
		  /SPEED 1x
		  /SPEED 2.4x (or 2,4x depending on regional settings)

/SPLIT <NONE | AUTO | CELLID | VOBID | CHAPTER | FILE | LAYER | 1GB>
	Used to tell the program when to split the programs output.
	Only applies to IFO and FILE modes.
	IFO mode supports the following options:
		NONE, AUTO, CELLID, VOBID, CHAPTER, LAYER, 1GB.
	FILE mode supports the following options:
		NONE, AUTO, CELLID, VOBID, FILE.

/NAMING <PGC> <ANGLE> (Append PGC and/or ANGLE information to file names)
	Used to tell the program to append PGC and/or ANGLE information to the file names when saving.
	Only applies to IFO mode.

/FILES <MOVIE> <ALL> "<File Name>" "<...>"
	Used to tell the program which file to select / deselect.
	Only applies to FILE mode.
	The '*' wildcard is supported. (ie. VTS*.VOB, VTS_01*.VOB, VTS_01_1.*, *.VOB)
		Note: Only 1 can be used per file name. (ie. VTS*.* WILL NOT WORK!!)
	Putting a '-' before a file name means it will be deselected instead of selected.
	Examples: /FILES MOVIE
		  /FILES MOVIE VIDEO_TS.*
		  /FILES VTS_01*
		  /FILES VTS* -*0.VOB
		  /FILES ALL -*.BUP -*0.VOB
		  /FILES MOVIE "VIDEO_TS.IFO" "VIDEO_TS.VOB"
		  /FILES ALL "-VIDEO_TS.VOB"

THE END