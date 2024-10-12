# This the writeup for the 2nd Question:
## 6-10-24
In this challenge, participants are provided with a single image, which depicts a spool of string. Upon inspecting the image with **binwalk**, no hidden data is found. <br>
However, a thorough examination using **exiftool** reveals an abundance of information. Notably, a user comment appears at line 36, below the focal length, stating: `trash2^3`.<br><br>

This comment serves as a critical hint. <br>
If participants recognize that the object in the image—a spool of string—can be interpreted as a clue, they will proceed to run the **strings** command on the image file:
---
![image](./string.jpg)
---
The output will yield numerous results, including the following:

```
strings string.jpg
deE@
r.HS
E#=7
!#@i
ZI*L
.
.
.
.
(over 2000 lines of strings)
UsO*
=VN#
d3RmQ1RGe1NwMDAxX29GX1lhcm59
```
Among these strings, the last entry is unusually long and noteworthy.<br>
If participants make the connection that `trash2^3` refers to Base64 encoding, they may attempt to decode this string.<br>

Successfully decoding the string will reveal the flag: ``wtfCTF{Sp001_oF_Yarn}``
