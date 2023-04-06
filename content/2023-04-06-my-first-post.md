+++
title = "My first post"
[taxonomies]
tags = [ "misc" ]
+++

It has been a while after I tried to build a webpage myself. The reason why I didn't explore this area is simply because building a webpage takes quite an efforts to learn and implement and obviously, time is not on my side. 

Testing a python code block

```python,linenos
import numpy as np
import pandas as pd
```

Testing math formula 
{{ katex(body="y=a+bx") }}
I have success fully add KaTex support for this theme. From now on I can use the <kbd>katex.html</kbd> short code to generate math symbols and equation. For example, we can use greek letter as {{ katex(body="\alpha")}} 

We can also write an equation using this
{% katex(block=true) %}f(x)=a+bx+cx^{2}{% end %}


Testing emoji
{{ kaomoji(label="shrug kaomoji", text="╮( ˘_˘ )╭") }}

Testing image embbeding

<a href="https://xkcd.com/2748">
<img src="https://imgs.xkcd.com/comics/radians_are_cursed.png" width="400"> <a>


[![Alt text](https://imgs.xkcd.com/comics/radians_are_cursed_2x.png)](https://xkcd.com/2748)
[![Alt text](https://imgs.xkcd.com/comics/coordinate_plane_closure_2x.png)](https://xkcd.com/2735)


<a href="https://xkcd.com/2748">Radian are cursed<a>
