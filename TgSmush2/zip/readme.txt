XWA TgSmush

This new TgSmush.dll allows to play high definition custom cutscenes.

See http://www.xwaupgrade.com/phpBB3008/viewtopic.php?f=9&t=11147


*** Requirements ***

This dll requires:
- Windows 7 or superior


*** Usage ***

To use this dll:

1) rename the original TGSMUSH.DLL to TgSmushOrig.dll
2) place the new TgSmush.dll and TgSmush.cfg next to it.

TgSmush.cfg is a config file. Open it with a text editor for more details.

The playable formats are .snm, .znm, .avi, .wmv and .mp4.

- snm and znm files are played with the original dll.
- avi files with a resolution <= 640x480 are played using AVIFile functions (Isildur's code).
- other avi files and wmv files are played using DirectShow.
- mp4 files are player using Media Foundation


The video data is shared via a file mapping.
The name is L"Local\\TgSmushVideo".
The pixel format is RGB32. 
The format of the data pointer is:
struct SharedMemData
{
    int videoFrameIndex;
    int videoFrameWidth;
    int videoFrameHeight;
    int videoDataLength;
    char* videoDataPtr;
};


*** License ***

XWA TgSmush is licensed under the MIT license. See LICENSE.txt


*** Source code ***

The source code of XWA TgSmush is situated at:
https://github.com/JeremyAnsel/xwa_TgSmush


*** Credits ***

- Defiant: his unfinished smush library has inspired Isildur
- Isildur: author of XWA Cutscene Replacer (XCR) 
- J�r�my Ansel (JeremyaFr)
