## [Natas](http://overthewire.org/wargames/natas/)

### Level 0
It is in source code.
 > Level 1: gtVrDuiDfck831PqWsLEZy5gyDz1clto

### Level 1
It is in source code again. Use console this time.
 > Level 2: ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi

### Level 2
This level was little tricky. The webpage says
 > There is nothing on this page.

Fair enough. Inspecting the source gives us a single pixel image file. I tried
inspecting the image data hoping to get the hidden password. But no luck.
Moving further, I noticed that the image file path is actually `files/pixel.png`.
Now connecting the dots : There is nothing on this page and files/ is accessible (perhaps?). Maybe there is something in `file/`. I was right. I found a suspicious file `users.txt` file
 
 > Level 3: sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14

### Level 3
This level was good. There were no direct clues except one comment in source code that says even Google can not find it. Hm give some thought. When can Google not crawl a website data? Obviously, when it has been blocked to do so. This blocking is accomplished by [Robots Exclusion Protocol](http://www.robotstxt.org/robotstxt.html). Now inspecting the robotx.txt file (which are public) i found that it looks like
```
User-agent: *
Disallow: /s3cr3t/
```
Hm clearly, there is something cooking in `s3cr3t/` directory. Digging further shows the directory contains `users.txt` file which has the password for next level. Phew. It was fun!

> Level 4: Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ

### Level 4
The levels are getting better. This one says authorised users should be coming from level 5. Wait. Does that even makes sense? We need to get obtain password for level 5 from level 4 and for that we need to visit level 4. But the page expects us to come from level5. Hm that is absurd. But giving a thought it is actually easy and doable. We can play with [HTTP referer](https://en.wikipedia.org/wiki/HTTP_referer). So basically we spoof the request.

We can easily [modify the headers](http://stackoverflow.com/a/29832996/3673031) and use [cURL](https://curl.haxx.se/docs/httpscripting.html) to send the requests. Changing the referer to `http://natas5.natas.labs.overthewire.org` did the job. The response was a neat html saying

>Access granted. The password for natas5 is iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq

>Level 5: iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq

