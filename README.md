# winChgSound
Powershell script used to change the Sound Output in Windows.

## :headphones::speaker: Usage

I use this to change the Windows 10 Sound Output between my headphones (which are plugged into my digital audio interface), and my speakers (which are plugged into the speaker jack of my desktop tower).

This saves me the time of doing: "Sound Settings" > "Choose your output device" > (choose the preferred output device) > Close

Includes two scripts and two batch files.

A batch file will call one of two scripts to change the "output device" in "Sound Settings". I use WinKey-R to run one of the two batch files (depending on which output device I want).

WinKey-R, "sndh" changes to headphones output (option 1)

WinKey-R, "snds" changes to speakers output (option 6)

You can change the option number in the Powershell scripts (.ps1 files) to whatever you want, depending on how your output settings are mapped.

![winChgSound.gif](img/winChgSound.gif)

## :turtle: Dependencies

This script uses the AudioDeviceCmdlets module for Powershell.

You can change the Index number (the second line of either ".ps1" file) to correspond with your output device in Sound Settings.

You can put the "winChgSound" folder into your username folder ("C:\Users\<your-username>\"), or alter the path in the ".bat" files to whatever you want.

The path for the folder containing the batch files and Powershell scripts must be added to Environment Variables in Windows. 

To add the folder path to Environment Variables: 
Run "sysdm.cpl" > Advanced tab > Environment Variables > select "Path" under System Variables > Edit > Add
