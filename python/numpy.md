---
description: description about numpy
---

# Numpy

## load, save npy

```text
import numpy as np

## load npy
r_npy = 'load_file.npy'
loaded_npy = np.load(r_npy)

## save npy
s_dist = np.arange(10)
s_npy = 'save_file.npy'
np.save(s_npy, s_dist)
```

## Array Slicing

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

## 要素ごとに処理-&gt;1Darray-&gt;2Darray

```text
all_distances = []

for x1, y1, z1 in zip(x_points, y_points, z_points):
    tmp_dist = []
    for x2, y2, z2 in zip(x_points, y_points, z_points):
        sub = np.array([x1, y1, z1]) - np.array([x2, y2, z2])
        distance = np.linalg.norm(sub)
        tmp_dist.append(distance)
```

