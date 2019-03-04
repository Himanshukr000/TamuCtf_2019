# Secrets(ANDROID)
## Description
![ks](ks.png)

Can you find my secrets?


Difficulty: Easy


Category: Android


## Writeup

Another easy challenge from tamuctf. This time it's android ... :P So we're given a .apk file to begin with. First thought when given a .apk challenge is to decode it using apktool. 
> apktool decode howdyapp.apk

It will create a directory howdyapp/ under which the standard android source files. Next is to look for the MainActivity.java inside the source files. Some Challenges have their flags inside the MainActivity.java file but this one had nothing. So I started looking for .xml files and got strings.xml under values/
which contained all the strings used in the app and there it was hiding behind the base64 encoding ... decoding it using
> echo Z2lnZW17aW5maW5pdGVfZ2lnZW1zfQ== | base64 -d

gave the flag 

# gigem{infinite_gigems}
