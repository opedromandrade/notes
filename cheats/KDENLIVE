### MY KDENLIVE RENDER PRESETS
## NAME » CRF » FPS

SPECTRUM » For audio spectrum videos. Radio rcordings
SCREEN » For audio screeen recording videos. Always choose 30fps for balanced cpu usage.
ViIDEO » For other video recordings. Always 60fps. CRF 18

SPECTRUM » 22 » 30 FPS
f=mp4 movflags=+faststart vaapi_device=/dev/dri/renderD128 vf=’format=nv12,hwupload’ vcodec=h264_vaapi threads=4 preset=faster progressive=1 g=15 bf=2 crf=%quality acodec=aac ab=128k

SCREEN » 20 » 30 FPS
f=mp4 movflags=+faststart vaapi_device=/dev/dri/renderD128 vf=’format=nv12,hwupload’ vcodec=h264_vaapi threads=4 preset=fast progressive=1 g=15 bf=2 crf=%quality acodec=aac ab=256k

SCREEN » 18 » 60 FPS
f=mp4 movflags=+faststart vaapi_device=/dev/dri/renderD128 vf=’format=nv12,hwupload’ vcodec=h264_vaapi threads=4 preset=medium progressive=1 g=15 bf=2 crf=%quality acodec=aac ab=384k

UNTESTED - source: https://archived.forum.manjaro.org/t/kdenlive-intel-gpu-acceleration-rendering-h264-video-boost-encoding/88829
f=mp4 movflags=+faststart init_hw_device=vaapi hwaccel=vaapi hwaccel_output_format=vaapi vaapi_device=/dev/dri/renderD128 vf='hwdownload,format=nv12|vaapi,hwupload' vcodec=h264_vaapi crf=20 real_time=-1 threads=4 preset=fast g=25 bf=2 acodec=aac ab=128k
