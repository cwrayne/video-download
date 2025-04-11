# How to Download Basically Any Video Ever (WIP)
A guide to download basically any video
## Prerequisites
 - [yt-dlp](https://github.com/yt-dlp/yt-dlp?tab=readme-ov-file#release-files)
 - m3u8 Grabber: [Chrome Web Store, may not work](https://chromewebstore.google.com/detail/mpccopnpamgaianficpdmidiamfcilid?utm_source=item-share-cb) [Unpacked zip](https://dashiellbenton.com/m3u8grabber/extension)
 - [FFmpeg](https://www.ffmpeg.org/download.html)

## Download a Video
### Most things
For all of the things in [here](https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md), you can do:
```
yt-dlp <url>
```
If you need to login, download Firefox if you haven't already, log in there, and then run this command:
```
yt-dlp <url> --cookies-from-browser firefox
```
Also for subtitles, add `--write-sub --write-auto-sub --sub-lang "en.*"` to the end of your command
### Some other things
Go to a video, refresh it, wait until the video starts playing, and then click on the extension that was in the prerequisites, the m3u8 grabber. Find the master.m3u8, or if its not there, do the top one. Copy the link for later. Then run in a terminal, where <url> is the m3u8 url you copied:
```
ffmpeg -i "<url>" -c copy -bsf:a aac_adtstoasc outputvideo.mp4
```
Then it will be in `outputvideo.mp4`.
### If none of those work
Just look up some stuff on reddit i guess. if your video isnt in the supportedsites.md, you can still *try* it, that doesnt mean it wont work
