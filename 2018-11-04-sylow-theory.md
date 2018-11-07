---
title: 
author: Colton Grainger
date: 2018-11-04
revised:
---

```
sage: count_elems = [80, 351, 3875, 5313]
sage: for i in count_elems:
....:     print (i, factor(i))
....:     
(80, 2^4 * 5)
(351, 3^3 * 13)
(3875, 5^3 * 31)
(5313, 3 * 7 * 11 * 23)
sage: small_index = [2205, 4125, 5103, 6545, 6435]
sage: for i in small_index:
....:     print( i, factor(i))
....:     
(2205, 3^2 * 5 * 7^2)
(4125, 3 * 5^3 * 11)
(5103, 3^6 * 7)
(6545, 5 * 7 * 11 * 17)
(6435, 3^2 * 5 * 11 * 13)
sage: normalizers = [1755, 5265]
sage: for i in normalizers:
....:     print( i, factor(i))
....:     
(1755, 3^3 * 5 * 13)
(5265, 3^4 * 5 * 13)
sage: playing = [4095, 4389, 5313, 6669]
sage: for i in playing:
....:     print(i, factor(i))
....:     
(4095, 3^2 * 5 * 7 * 13)
(4389, 3 * 7 * 11 * 19)
(5313, 3 * 7 * 11 * 23)
(6669, 3^3 * 13 * 19)
sage: factor(9555)
3 * 5 * 7^2 * 13
```
