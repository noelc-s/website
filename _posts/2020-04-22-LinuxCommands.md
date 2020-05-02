---
layout:     post
title:		Code Snippets
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

## Zathura
### Change page aligning
{% highlight bash %}
:set first-page-column 1:1
{% endhighlight %}

## Matlab
### Fullscreen Figure
{% highlight matlab %}
fig = figure('units','normalized','outerposition',[0 0 1 1]);
{% endhighlight %}

### Proper Formatting
{% highlight matlab %}
xlabel('$\theta_1$','interpreter','latex')
ylabel('$\theta_2$','interpreter','latex')
zlabel('$\theta_3$','interpreter','latex')
set(gca,'TickLabelInterpreter', 'latex');
set(gca,'FontSize',17)
set(gca,'linewidth',2)
{% endhighlight %}