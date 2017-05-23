# FFMPEG-Samples
Useful samples of ffmpeg console commands

## Split video file to images (frames) with timestamp
ffmpeg -i c:\path\to\file.mp4 -vf "drawtext=fontfile=Vera.ttf: text='%{pts\:hms}': x=(w-tw)/2: y=h-(2*lh): fontcolor=white: fontsize=70: box=1: boxcolor=0x00000000@1" c:\path\to\images\image%03d.png

Notices:
1) You should invoke it from folder with ffmpeg or ffmpeg should be added to PATH environement variable.
2) You should have Vera.ttf font file.
3) c:\path\to\images\ should exist.
