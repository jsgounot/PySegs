PySegments
==========

Short module designed to work with arithmetic windows. Quick example

Example 
-------

```python

Segment(40, 60) + Segment(50, 70) # -> SegList([Segment(40 - 70)])
Segment(40, 60) - Segment(50, 70) # -> SegList([Segment(40 - 50)])

SegList([Segment(15, 25), Segment(60, 80), Segment(35, 40)]) + Segment(10, 38) # -> SegList([Segment(10 - 40), Segment(60 - 80)])
SegList([Segment(15, 30), Segment(35, 40), Segment(60, 80)]) - Segment(20, 70) # -> SegList([Segment(15 - 20), Segment(70 - 80)])
```
