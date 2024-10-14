# Wh3rE the Sun D0nt sh1n3
## 11/10/24:

---
## Question Statement:
```
1010011001 10000011
where does the light of a candle not reach?
```
This consists of two binary encoded numbers, corresponding to ``665`` and ``131``.
The next line is indicative of the fact that the answer to this question is in the image file.

![Candle Image](./pexels-nicolas-langellotti-28179636-18128539.jpg)

---
## Approach:

There is a simple image file for the replacement, that and the question text, mentioned in the original documentation for q1.<br>
the image given here has been used to hide a txt file ``candle.txt``.<br>
using steghide and no password, the file can be extracted.<br>
```
steghide extract -sf pexels-nicolas-langellotti-28179636-18128539.jpg -p ""
wrote extracted data to "candle.txt".
```
you can know for sure it is not a simple txt file if you run:
```
file candle.txt
candle.txt: Netpbm image data, size = 345 x 91, rawbits, pixmap
```
after extracting if you convert it to ppm format, by simply renaming it to ``candle.ppm``<br>
you can open it in a text editor like vim, and use the decoded binary numbers as pixel dimesions<br>
inputting replacing the nonsense pixel count will get you the flag.<br>

```
vim candle.ppm
```
we can notice that the pixel count is ``345`` and ``91``
This needs to be replced by the ``665`` and ``131`` we have decoded from binary
changing the pixel count to the decoded one by editing the file in vim gives us an updated image.
Opening this image gives a sensible output image, which is ``wtfCTF{Und3r_1t}``
