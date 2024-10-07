# This the writeup for the 2nd Question:
## 6-10-24
So, we give them only 1 image, and maybe a hint/directive type question.
the image on opening is just a spool of string. 
On doing binwalk, you find nothing, as there is nothing there.
On doing exiftool, there is an overload of information, but if you look for user comment (at line 36 below focal length) you can see the comment says trash2^3. 
What does that mean?
If they make of the image, that the object in the image (string) is in itself a hint, they will run string on the image
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
The last string is unusually long, hmm.
If their mind clicks and they realise that trash2^3 is referring to bin64 encryption, they will try to decrypt it.
Leading to the flag ``wtfCTF{Sp001_oF_Yarn}``
