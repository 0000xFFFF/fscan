# fscan - file (duplicates) scanner/searcher (C#, console)
- Easily: find duplicate files / compare files.

## DOWNLOAD
\[[here](https://github.com/0xC0LD/fscan/raw/master/fscan/fscan/bin/Release/fscan.exe)\]

## HELP
> fscan
```
 +===[ ABOUT ]
 | ABOUT.....: compare/scan/id files
 | AUTHOR....: 0xC0LD
 | BUILT IN..: VS C# .NET 4.5
 | VERSION...: 35
 | USAGE.....: fscan.exe <file/command> <command2> <cmd3> <cmd4> ...

 +===[ STANDARD OPTIONS ]
 | +==[ FIND DUPLICATE FILES (FDF) ]
 | | name    = find duplicate files by name.ext
 | | noext   = find duplicate files by name
 | | hash    = find duplicate files by md5 checksum hash
 | | hashbuf = find duplicate files by md5 checksum hash, but use a larger byte buffer (1 mil bytes) (faster)
 | | hashexe = find duplicate files by md5 checksum hash, but use the 'md5sum.exe' to get the file hash
 | | byte    = find files that have the same byte size
 | | pic     = find duplicate images (resize image to 16x16 -> compare pixels)
 | | pic2    = find duplicate images (resize image to 16x16 -> average out the RGB -> compare pixels)
 |
 | +==[ FIND FILES THAT ___ (FFT) ]
 | | vid     = find corrupt and playable videos (uses ffmpeg)
 | | vidt    = find playable video files (uses ffmpeg)
 | | vidf    = find corrupt video files (uses ffmpeg)
 | | sound   = print video files that have, and don't have sound/audio (uses ffprobe)
 | | soundt  = find video files that have sound/audio (uses ffprobe)
 | | soundf  = find video files that don't have sound/audio (uses ffprobe)
 | | long    = find files with over 260 characters in file path (too long)
 | | md5name = find files with a MD5 hash name

 +===[ RUNTIME OPTIONS / OPTIONS WHILE PROCESSING ]
 | all      = also scan subdirectories
 | del      = send the found file to recycle bin
 | mov      = move the found file to a folder (fscan_dir)
 | statXXXX = print status every XXXX ms
 |
 | +==[ FDF ]
 | | 1     = use the first file (del/mov/...)
 | | 2     = use the second file (del/mov/...) (default)
 | | ask   = when a dupe is found prompt on what to do with the files
 | | end   = print/process files when the file scanning/comparing is finished
 | | nomd5 = don't calculate/print the md5 checksum of files

 +===[ PRINT ONLY OPTIONS / SORT OPTIONS ]
 | sizea    = print file sizes in ascending order
 | sized    = print file sizes in descending order
 | dsizea   = print directory size in ascending order
 | dsized   = print directory size in descending order
 | dcounta  = print directory files count in ascending order
 | dcountd  = print directory files count in descending order
 | rdcounta = print directory (+subdirs) files count in ascending order
 | rdcountd = print directory (+subdirs) files count in descending order
 | datea    = print file creation dates in ascending order
 | dated    = print file creation dates in descending order
 | lena     = print video length in ascending order (uses ffprobe)
 | lend     = print video length in descending order (uses ffprobe)

 +===[ OPTION_ = use multithreading (extremely fast, experimental, not finished) ]
 | name_, noext_, hash_, hashbuf_, hashexe_, byte_, pic_, pic2_
 | vid_, vidt_, vidf_, sound_, soundt_, soundf_,
 | lena_, lend_
```

## EXAMPLES
```
> fscan hash              = just print files that are the same
> fscan hash all del      = find files that are the same and send the second file to the recycle bin
> fscan soundf del        = find videos that have no sound and delete them
> fscan pic all mov 1     = find duplicate images and move the first file
```