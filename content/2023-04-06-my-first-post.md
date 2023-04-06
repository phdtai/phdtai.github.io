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
I have success fully add KaTex support for this theme. From now on I can use the <bkd>katex.html<bkd> short code to generate math symbols and equation. For example, we can use greek letter as {{ katex(body="\alpha")}} 

We can also write an equation using this
{% katex(block=true) %}f(x)=a+bx+cx^{2}{% end %}


Testing emoji
{{ kaomoji(label="shrug kaomoji", text="╮( ˘_˘ )╭") }}