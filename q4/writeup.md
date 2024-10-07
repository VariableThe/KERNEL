# Writeup for question:-
## 5-10-24
So, this question is presented in the form of an Image and an cisco packet tracer diagram? thats the hint.
the image is divided into 3 differnt sections as is visible in ``new_q4.png`` .
The image seems blanck at first untill you realise that the hints point toward three RGB values.
These values are:
```
170,183,198

098,201,235

129,158,076
```
these values are important when they realise that the RGB values are the values of the color of the text that is hidden in the image.
Now the trick to this question is that the text is highlighted in such a way that the highlight color is just one off the text color, making the change invisible to the naked eye.
But if they find a software or online tool to extract the text based on the RGB values like this [site](https://onlinepngtools.com/extract-color-from-png)
Like I did in the process.png image.
They have to get the codes and find the individual parts of the flag and string them together to form ``wtfCTF{Sp3ctrum5_0f_rea1ity}``
