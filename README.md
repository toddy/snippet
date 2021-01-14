# Shell commands

## Videokorrekturen

### Ton ist schneller als das Bild
```
ffmpeg -i Inputvideo.mp4 -itsoffset 0.5 -i Inputvideo.mp4 -c:a copy -c:v copy -map 0:v:0 -map 1:a:0 outVideo.mp4
```

### Bild ist schneller als der Ton
```
ffmpeg -i Inputvideo.mp4 -itsoffset 2 -i Inputvideo.mp4 -c:a copy -c:v copy -map 0:a:0 -map 1:v:0 outVideo.mp4
```

```
-itsoffset ZAHL in Sekunden z.B. 1 oder 0.5
-map 1:a:0 oder -map 1:v:0 je nachdem ob man Ton (audio) oder Bild (video) nach hinten verschieben will.
```
