# unpackTunes
Windows PowerShell script to unpack randomly named music files and places them in folders by artist/album/title.
Script takes required input and output directory. For the input folder, it can have subfolders which the script will traverse.

## Sample folders

```
:open_file_folder: c:\temp\tunes
  :open_file_folder: F00
    :camera: ADAN.m4a
    :camera: BFVQ.mp3
  :open_file_folder: F01
    :camera: ALSR.mp3
    :camera: PTZX.m4p
```

## PowerShell command prompt examples
```powershell

> .\ unpackTunes.ps1 -musicSource C:\temp\tunes -musicDestination c:\music
#
# overwrite existing files
> .\ unpackTunes.ps1 -musicSource C:\temp\tunes -musicDestination c:\music -force
#
# remove the word "The" from artist name, such as "The Beatles" becomes "Beatles"
> .\ unpackTunes.ps1 -musicSource C:\temp\tunes -musicDestination c:\music -removeTheFromArtist -force

```

## Parameters
Parameter | Description
--------- | -------------
musicSource | Required folder or root folder for location of randomly named music files
musicDestination | Required target folder to copy files to
removeTheFromArtist | remove the starting "The" from artist name, such as "The Beatles" becomes the "Beatles"
force | overwrite existing files


