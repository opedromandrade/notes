Framerate in all cases 30fps
The "-y" is a tag to automatically overwrite any existng file 

Case #01
» Simple recording with NO HardWare acceleration and NO sound

$ ffmpeg -f gdigrab -framerate 30 -i desktop -f dshow -c:v libx264rgb -crf 0 -preset ultrafast -color_range 2 output_video.mp4

Case #02
» Simple recording with NO HardWare acceleration WITH sound

$ ffmpeg -f gdigrab -framerate 30 -i desktop -f dshow -i audio="Device (NameOfDevice)" -c:v libx264rgb -crf 0 -preset ultrafast -color_range 2 output_video.mp4

Case #03
» Recording script USING Intel HardWare acceleration and NO sound

$ ffmpeg -y -rtbufsize 300M -f gdigrab -probesize 30M -framerate 30 -i desktop -c:v h264_qsv -pixel_format yuv444p -b:v 8M output_video.mp4



Open WebCam
$ ffplay -f dshow -framerate 30 -i video="USB 2.0 Camera "

Open WebCam VGA mode
$ ffplay -f dshow -framerate 30 -video_size 640x480 -i video="USB 2.0 Camera "

$ ffplay -f dshow -framerate 30 -video_size 320x240 -i video="USB 2.0 Camera "


Get ffmpeg
https://ffmpeg.org/download.html

Get ffmpeg for windows
https://www.gyan.dev/ffmpeg/builds/ffmpeg-git-essentials.7z

ffmpeg info
https://trac.ffmpeg.org/wiki/DirectShow
https://trac.ffmpeg.org/wiki/Capture/Desktop
https://trac.ffmpeg.org/wiki/Hardware/VAAPI
https://trac.ffmpeg.org/wiki/Encode/H.264
