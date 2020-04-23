---
layout:     post
title:		Linux Commands
subtitle:   That Have Come in Handy
author:     Noel Csomay-Shanklin
tags: 		Reading
category:   PersonalReading
---
## Table of Contents
* TOC
{:toc}

## Video Compression
{% highlight bash %}
ffmpeg -r ~FramesPerSecond~ -i Input.avi -y -an -c:v libx264 -preset veryslow -qp 0 -vf "pad=ceil(iw/2)*2:ceil(ih/2)*2" Output.mp4 -vf "pad=ceil(iw/2)*2:ceil(ih/2)*2"
{% endhighlight %}