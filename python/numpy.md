---
description: description about numpy
---

# Numpy

行列 -&gt; 縦横

```text
>>> import numpy as np
>>> a = np.arange(10)
>>> a
array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
>>> a[1:5]
array([1, 2, 3, 4])
>>> a[::-1] #逆順
array([9, 8, 7, 6, 5, 4, 3, 2, 1, 0])
>>> a[:3]
array([0, 1, 2])
>>> a[::2] #1つ置き
array([0, 2, 4, 6, 8])
```

