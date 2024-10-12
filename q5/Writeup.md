# Writeup
## 10/10/24
<br><br>
## Question statement:-

A secretive agent sent a message to a colleague, hoping to convey important information without arousing suspicion. The message reads: ``"Z0x_ai11_t0F_qhv3_cL3_q1Q."`` The sender used their phone, which has the number ``13406997094``.

Your task is to uncover the hidden PIN within the message. Can you decipher it and reveal the PIN?

Provide the answer in the format: ``wtfCTF{PIN}``.

<br> <br>

## Approach

The message sent is ``Z0x_ai11_t0F_qhv3_cL3_q1Q`` <br>
This is encrpted via the gronsfield cipher using the sender's number which is: ``13406997094``<br>
Decrypting this using the cipher gives us `` Y0u_wi11_n0W_hav3_tH3_p1N``<br>
Which is indicative of the fact the the pin has been trasnlated to the sender in the message itself.<br>
A photo attached will indicate that the sender uses a phone with a numpad.<br>
The pin is the sum of all the multitap codes for the letters of the message that was sent.<br>
The multi tap code comes to: ``999 88 9 444 66 9 44 2 888 8 44 7 66``<br>
Adding all of these gives us: ``2674``<br>
Which is the pin that will be used in the flag.<br>
