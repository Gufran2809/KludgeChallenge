# Answer

"**weeb{omaewa_M0u_shinderu}**"

# Concepts involved
the challenge is to brush few basics of cryptography,which include
 - base64 encryption
 - base32 encryption
 - cracking hashes 
 - vigenere cipher

# Solution

1. Download the zip file.

2. If you have gone through the hint and done some googling you'll understand the passphrase for kenshiro.jpg is "**nani**"

3. On using the steghide on kenshiro.jpg you'll get a new file named 2.txt .

4. Now you should have 1.txt ,2.txt ,3.txt and 4.jpg

5. On viewing the 1.txt you'll find
```html
  d2VlYns=
```
which by an '**=**' at end and letters in lower case can be guessed to be encrypted in base64.

6. Use your favorite base64 decryter online and you'll get
```html
  weeb{
```
attaboy gettin close to flag.

7.  Now 2.txt will give the another part , and it provides a hint i.e '**nani**' in english ,which is '**what**'

8. And by looks of having a key and an encpted message i'd first prey on vigenere cipher.

9.  Which on decrypting
   ```html
     ktaxsh
   ```
   gives 
   ```
omaewa
```
10. Now for the 3rd part the file reads
```html
L5GTA5K7
```
which has only Uppercase letters ,and my first guess would be to decrypt it with base32.

Again use your favorite base32 decrypter and you'll find the message 
```
_M0u_
```
11. Now final part open the image file , what do you see a #, some random gibberish and a rainbow.

12. I don't it would take any moment for anyone with even little knowledge of hash to realize what it is.

13. crack the hash with any hashkiller. I use [crackStation](https://crackstation.net/)

14. The last part will read
```
shinderu}
```

16. On join all the hardearned strings ull get the flag "**weeb{omaewa_M0u_shinderu}**".
