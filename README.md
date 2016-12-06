# ffmpeg-commands
My List of ffmpeg commands

__12-06-2016__  
_Convert a bunch of wmv files to browser-compatible mp4 files in Windows_  
```bash
@ECHO OFF
FOR %%a IN ("*.wmv") DO ( ffmpeg -y -i "%%a" -c:v libx264 -preset slow -crf 18 -c:a libvo_aacenc -q:a 5 -pix_fmt yuv420p "mp4\%%~na.mp4" &  move "%%a" converted )
```
