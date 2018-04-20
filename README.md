PySegments
==========

PySegments is a short module designed to make windows analysis easier. This module is composed of two objects : `Segment` and `SegList` allowing you to easily compare and manage several windows at the same time. 

Quick example 
-------------

```python
from segments import Segment, SegList

Segment(40, 60) + Segment(50, 70) # -> SegList([Segment(40 - 70)])
Segment(40, 60) - Segment(50, 70) # -> SegList([Segment(40 - 50)])

SegList([Segment(15, 25), Segment(60, 80), Segment(35, 40)]) + Segment(10, 38) 
# -> SegList([Segment(10 - 40), Segment(60 - 80)])
SegList([Segment(15, 30), Segment(35, 40), Segment(60, 80)]) - Segment(20, 70) 
# -> SegList([Segment(15 - 20), Segment(70 - 80)])
```

Other examples
--------------

```python
s1 = Segment(0, 40)
s12 = Segment(0, 40)
s2 = Segment(0, 20)
s3 = Segment(30, 50)

5 in s1 # -> True
s1 in s2 # -> True
s1.overlapp_count(s2, prc=False) # -> 20
s1.overlapp_count(s2, prc=True) # -> 50%

sl1 = SegList([s2, s3])
s1 in sl1 # -> True
s1.overlapp_count(sl1, prc=True) # -> 75%
```
