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

<div class="notes">

Speaker notes go here.

</div>

## Template for figures

![](figures/00_template-vector-images/drawing-v00.svg)

<div class="notes">

Speaker notes go here.

</div>

## Template for tabsets

<div class="panel-tabset">

### Tab A

Content for `Tab A`

### Tab B

Content for `Tab B`

</div>

<div class="notes">

Speaker notes go here.

</div>

## Template for tabsets with code-blocks

<div class="panel-tabset">

### Code-block A

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

### Code-block B

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

</div>

<div class="notes">

Speaker notes go here.

</div>

## Multiple columns

<div class="columns">

<div class="column" width="50%">

Left column

</div>

<div class="column" width="50%">

Right column

</div>

</div>

<div class="notes">

Speaker notes go here.

</div>

## Multiple columns with code-blocks

<div class="columns">

<div class="column" width="50%">

``` python
#Left column
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

</div>

<div class="column" width="50%">

``` python
#Right column
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

</div>

</div>

<div class="notes">

Speaker notes go here.

</div>

## :construction: Line Highlighting (10 lines)

<div class="code-with-filename">

**matplotlib.py**

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

</div>

<div class="notes">

Speaker notes go here.

</div>

## :construction: Line Highlighting (N lines)

``` python
import datetime
import unittest

import pandas as pd
import pandas_datareader.data as web

def get_stock_data(ticker):
    """pull data from stooq"""
    df = web.DataReader(ticker, 'yahoo')
    return df

class TestGetStockData(unittest.TestCase):
    @classmethod
    def setUpClass(self):
        """We only want to pull this data once for each TestCase since it is an expensive operation"""
        self.df = get_stock_data('^DJI')

    def test_columns_present(self):
        """ensures that the expected columns are all present"""
        self.assertIn("Open", self.df.columns)
        self.assertIn("High", self.df.columns)
        self.assertIn("Low", self.df.columns)
        self.assertIn("Close", self.df.columns)
        self.assertIn("Volume", self.df.columns)

    def test_non_empty(self):
        """ensures that there is more than one row of data"""
        self.assertNotEqual(len(self.df.index), 0)

    def test_high_low(self):
        """ensure high and low are the highest and lowest in the same row"""
        ohlc = self.df[["Open","High","Low","Close"]]
        highest = ohlc.max(axis=1)
        lowest = ohlc.min(axis=1)
        self.assertTrue(ohlc.le(highest, axis=0).all(axis=None))
        self.assertTrue(ohlc.ge(lowest, axis=0).all(axis=None))

    def test_most_recent_within_week(self):
        """most recent data was collected within the last week"""
        most_recent_date = pd.to_datetime(self.df.index[-1])
        self.assertLessEqual((datetime.datetime.today() - most_recent_date).days, 7)

unittest.main()
```

<div class="notes">

Reference for the code!

https://machinelearningmastery.com/a-gentle-introduction-to-unit-testing-in-python/

</div>

## :video_camera: Embedding Yotube Video

<https://www.youtube.com/embed/hbf7Ai3jnxY>

<div class="notes">

Available aspect ratios include 1x1, 4x3, 16x9 (the default), and 21x9.

Further details to render videos
https://quarto.org/docs/authoring/videos.html

</div>

<!--
adding HTML comment syntax to not render the following lines
## Embedding a video.mp4 {background-video="video.mp4" background-video-loop="true" background-video-muted="true" background-opacity=0}
-->
