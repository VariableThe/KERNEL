# Replacement Question without stegsuite.
## 11/10/24:

There is a simple image file for the replacement, that and the question text, mentioned in the original documentation for q1.<br>
the image given here has been used to hide a txt file ``candle.txt``.<br>
using steghide and no password, the file can be extracted.<br>
```
steghide extract -sf pexels-nicolas-langellotti-28179636-18128539.jpg -p ""
wrote extracted data to "candle.txt".
```
after extracting if you convert it to ppm format, by simply renaming it to ``candle.ppm``<br>
you can open it in a text editor like vim, and use the decoded binary numbers as pixel dimesions<br>
inputting replacing the nonsense pixel count will get you the flag.<br>
