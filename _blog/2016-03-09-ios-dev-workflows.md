---
title: "iOS Development Workflows"
tags: ["swift","ios","workflow","developer tools"]
published: false
---

Install [ffmpeg](https://www.ffmpeg.org). I prefer to use [homebrew](http://brew.sh) to manage my packages:

```
brew install ffmpeg
```

```
width=1080
height=1920
ffmpeg -i in.mp4 -filter:v "scale=iw*min($width/iw\,$height/ih):ih*min($width/iw\,$height/ih), pad=$width:$height:($width-iw*min($width/iw\,$height/ih))/2:($height-ih*min($width/iw\,$height/ih))/2" out-1080x1920.mp4
```