# Drag'n'Compress
Author: Nils Badtke + dima

## Description
Compress videos with FFmpeg made easy with drag'n'drop.

![drag&drop demo](https://user-images.githubusercontent.com/35294329/223697294-fe93649f-05fb-4a4f-8cd3-79e3b0b7cff3.gif)

---

![before](https://user-images.githubusercontent.com/35294329/223697409-401d8bef-4e78-4295-9fa9-feb517e3cadb.png)

---

![after](https://user-images.githubusercontent.com/35294329/223697544-8b48547f-9eb4-43f1-80ed-b18c34e5575e.png)

## System requirements
**OS:** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Microsoft Windows 7 or above (due to the use of Powershell)*  
**Hardware:** &nbsp;*Runs on almost anything. In general, the better the hardware, the faster the compression process.*

## Installation
1. [Download a release package.](https://github.com/dima333750/Drag-n-Compress-video/releases)  
   > A release package is self-contained. That means FFmpeg is included in a release package. There are no requirements to be met.  
   > Currently used version of [FFmpeg](https://ffmpeg.org/): [`Codex FFmpeg v5.1.2-full_build`](https://github.com/GyanD/codexffmpeg/releases/tag/5.1.2)
1. Unzip the downloaded package to a location of your choice.
1. Run `install.ps1` by right-clicking `install.ps1` and select "Execute with PowerShell...".

## Usage
After running the installation script, you can simply drag'n'drop (drag and drop) the video file(s) onto `dragAndDropVideoFileHere.ps1`.  
You can also create one or more shortcuts to `dragAndDropVideoFileHere.ps1` anywhere and drag'n'drop the video file(s) onto the shortcut(s).
Use additional pre-installed files. GPU AMD Acceleration are fast, but reduce the quality.

### Advanced usage
It is possible for video files to contain multiple audio tracks.
This is often used in screen recording to separate individual sound sources, for example microphone and game.

The script in v1.0.0 merges all audio track into one.

It is possible to spare the first and/or the last track.

To do that, go into the file `dragAndDropVideoFileHere.ps1` and alter the values in the lines 25 and or 26:
```
[bool] $omitFirstAudioTrack = 0
[bool] $omitLastAudioTrack = 1
```
`0` means deactivate
`1` means activate
