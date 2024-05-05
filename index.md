# Real-time AI for surgery with NVIDIA-Holoscan platform
Miguel Xochicale

# 

<div style="background-color: rgba(22,22,22,0.75); border-radius: 10px; text-align:center; padding: 0px; padding-left: 1.5em; padding-right: 1.5em; max-width: min-content; min-width: max-content; margin-left: auto; margin-right: auto; padding-top: 0.2em; padding-bottom: 0.2em; line-height: 1.5em!important;">

<span style="color:#939393; font-size:1.5em; font-weight: bold;">Real-time
AI for surgery</span>  
<span style="color:#939393; font-size:1.5em; font-weight: bold;">with
NVIDIA-Holoscan platform</span>  
<span style="color:#777777; font-size:1.2em; font-weight: bold;"></span>  
<span style="padding-bottom: 0.5rem;"><br> </span>  
[](http://mxochicale.github.io/) Miguel Xochicale, PhD  
<span style="border-bottom: 0.5px solid #00ccff;">[
`mxochicale/`](https://github.com/mxochicale/real-time-ai-for-surgery-with-NVIDIA-Holoscan-platform)</span>

</div>

<div class="footer">

<span class="dim-text" style="&quot;text-align:left;'">2024-04-20 @
[Link for grid-worms-animation
2023](https://github.com/saforem2/grid-worms-animation/)</span>

</div>

# Overview

1.  [overview](#sec-ov)
2.  [holoscan-platform](#sec-hp)
3.  [end-to-end-apps](#sec-e2e)
4.  [demos](#sec-demos)
5.  [aob](#sec-aob)

## Template for figures

<div id="sec-hp">

![](figures/00_template-vector-images/vectors/drawing-v00.svg)

</div>

## Template for tabsets

<div class="panel-tabset">

### Tab A

Content for `Tab A`

### Tab B

Content for `Tab B`

</div>

## Multiple columns

<div class="columns">

<div class="column" width="40%">

Left column

</div>

<div class="column" width="60%">

Right column

</div>

</div>

## Line Highlighting

``` python
import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(subplot_kw={'projection': 'polar'})
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```
