---
layout: post
title: "In search of the nicest colormap"
subtitle: "Pretty, colorful, useful, versatile, perceptually uniform..."
date: 2021-07-03 09:24:00 +0200
tags: [Random thoughts]
background: '/img/posts/marc-schulte-KJCyvlA_aAQ-unsplash.jpg'
published: true
---

<!-- https://unsplash.com/photos/KJCyvlA_aAQ -->
<!-- https://unsplash.com/photos/mz471WAXhCU -->

I've always been quite fond of the colors used in the spectral frequency display of [Adobe Audition](https://www.adobe.com/se/products/audition.html). It looks quite pretty and the colors are also very helpful in discerning small differences in intensity. 

<img class="img-fluid" src="/img/posts/audition.jpg" alt="Screenshot">

Recently, I came accross a fascinating presentation about the work behind some new colomaps for [Matplotlib](https://matplotlib.org/). They set out to develop some colormaps that are colorful, pretty, sequential, perceptually uniform, black-and-white compatible and accessible to colorblind viewers. The video also includes a fascinating crash course in color theory. Highly recommended.

<!-- https://www.w3schools.com/howto/howto_css_responsive_iframes.asp -->
<div style="position:relative;overflow:hidden;width:100%;padding-top:56.25%;">
<iframe style="position:absolute;top:0;left:0;bottom:0;right:0;width:100%;height:100%;" src="https://www.youtube.com/embed/xAoljeRJ3lU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

The colormaps magma, inferno, plasma and viridis and the tools [colorspacious](https://pypi.org/project/colorspacious/) and [viscm](https://pypi.org/project/viscm/) that they developed are described [here](https://bids.github.io/colormap/) and [here](https://github.com/bids/colormap). The colormaps are visualized below.

```
python -m viscm view magma --save magma.png --quit --uniform-space buggy-CAM02-UCS
```
<img class="img-fluid" src="/img/posts/magma.png" alt="Screenshot">

```
python -m viscm view inferno --save inferno.png --quit --uniform-space buggy-CAM02-UCS
```
<img class="img-fluid" src="/img/posts/inferno.png" alt="Screenshot">

```
python -m viscm view plasma --save plasma.png --quit --uniform-space buggy-CAM02-UCS
```
<img class="img-fluid" src="/img/posts/plasma.png" alt="Screenshot">

```
python -m viscm view viridis --save viridis.png --quit --uniform-space buggy-CAM02-UCS
```
<img class="img-fluid" src="/img/posts/viridis.png" alt="Screenshot">

I also found some quite pretty colormaps in the [cmocean](https://matplotlib.org/cmocean/) package, such as [thermal](https://matplotlib.org/cmocean/#thermal) and [ice](https://matplotlib.org/cmocean/#ice).

```python
from viscm import viscm
import cmocean
viscm(cmocean.cm.thermal)
```
<img class="img-fluid" src="/img/posts/thermal.png" alt="Screenshot">

```python
from viscm import viscm
import cmocean
viscm(cmocean.cm.ice)
```
<img class="img-fluid" src="/img/posts/ice.png" alt="Screenshot">

Returning to the colors used in the spectral frequency display of Adobe Audition, 

```
python -m viscm edit
```

The search continues... :telescope: :smiley:
