# Writeup For Question 1 (includes approach):
## 1-10-25
## Question Statement:
```
10010110000 10010101111
where is the light of the candle the most absent?
```
This consists of two binary encoded numbers, corresponding to '1200' and '1199'.
The next line is indicative of the fact that the answer to this question is in the txt file.

## Approach:

Converting the binary to decimal you get '1200' and '1199', initialy these seem like random numbers.
If the hint is understood properly, the contestant will run binwalk on the txt file:
```
binwalk finalQ.txt
```
In this they will get to know of a zip file.
Extracting it using
```
binwalk -e finalQ.txt
```
extracts the contents into a folder.

Opening the folder, we can see a scrambled image titled image.ppm
opening this image in vim (after navigating into the extracted folder)
```
vim image.ppm
```
we can notice that the pixel count is '120' and '199'
This seems similar to the '1200' and the '1199' we have decoded from binary
changing the pixel count to the decoded one by editing the file in vim gives us an updated image.
Opening this image gives a sensible output image, where I believe the flag can be stored through steganography, presently the image is that of a cat.