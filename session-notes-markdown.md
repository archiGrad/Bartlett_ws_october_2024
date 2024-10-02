# Session: 1/10/2024

## To Do:
1. Find a site in distress:
   - Examples: bridge, rooftop, hallway, family house, etc.
   - Distress can mean many things (e.g., underuse, bad location)

## Before You Go:
- Ensure cellular and location are turned on on GSM
- Map your entire route:
  - Capture 30+ images of misuse, leaks, annoying stoplights, etc. (negative or positive)

## Photogrammetry Video:
- Create a 1-minute video on cellphone
- Tips:
  - Smooth video, no sudden zoom-ins or movements
  - Avoid reflective surfaces like glass
  - Ensure a lot of overlap, don't zoom in too much
  - Walk around, don't stand still and rotate (this won't work)
  - Most tutorials cover images, but film is fine
  - Example of a good photogrammetry video (though tragic): [YouTube Video](https://www.youtube.com/watch?v=sBw0hZBlOu0)

## Additional Tasks:
- Go over the rest of the Houdini foundations file
- Play around with some of the nodes, params, etc.

---

# Session: 2/10/2024

## Planning:
1. Houdini recap?
2. Site discussion:
   - Did images work?
   - Did video work?
   - Did KML/trajectory work?
3. Check image metadata:
   ```
   magick identify -verbose "image.jpg"
   ```
   *Tip: Convert images:
   ```
   magick mogrify -format .jpg *.HEIC
   ```
4. Extract frames from video:
   ```
   ffmpeg -i input.mp4 -vf fps=1 -q:v 1 output_%04d.jpg
   ```
5. Download images from YouTube:
   ```python
   from pathlib import Path
   from pytube import YouTube

   imgpath = Path("project/images")
   imgpath.mkdir(exist_ok=True)
   url = "https://www.youtube.com/watch?v=sBw0hZBlOu0"
   yt = YouTube(url)
   video = yt.streams.get_by_itag(157)
   video.download()
   for i in yt.streams:
       print(i)
   ```
6. Download RealityCapture and do photogrammetry
7. Load in Houdini and extract cameras:
   ```c
   for(int i = 0; i < npoints(0); i++){
       if(i % 8 == 0){
           // calc center pos and add point
           vector posA = lerp(point(0,"P",i-6),point(0,"P",i-8),0.5);
           int newpnt = addpoint(0, posA);
           
           // calculate the normal vector
           vector posB = lerp(point(0,"P",i-1),point(0,"P",i-3),0.5);
          
           vector N = posB - posA;
           setpointattrib(0,"N", newpnt,- N *100, "set");
           setpointattrib(0,"up", newpnt, up, "set");
       } 
   }
   ```
8. Form groups
