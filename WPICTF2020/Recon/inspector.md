# inspector

> my sources tell me that the flag might be at wpictf.xyz

> made by: acurless and awg




When looking at the source code of the page wpictf.xyz, we can find a comment that say

> <!-- If you are looking for a WPI{FLAG}, you CANT be a robot! --> 

 
A quick search about web robot teach me that web robot can't acess adress refered in the file robots.txt of a website.
By going to wpictf.xyz/robots.txt, we can read the text
>   User-agent: * Disallow: /inspector.txt

If we need to go were "robots can't go", we need to go to the URL wpictf.xyz/inspector.txt
There we can read the following text:
>  I heard that the WPICSC club webpage may be of use to you.

A quick google search give us the following website for WPICSC (cybersecurity club)
  https://web.cs.wpi.edu/~csc/

In it's source code, we can find a comment next to the CTF Manager name:
>  <p><b>CTF Manager: </b>Adrian Curless<br> <-- Check out our prizes-->
  
 So, if we go to the source code of the page https://ctf.wpictf.xyz/prizes, we can finally get the comment:
>   <!--WPI{1nsp3ct0r\_H@ck3R} -->
   
 **flag** : WPI{1nsp3ct0r\_H@ck3R}
