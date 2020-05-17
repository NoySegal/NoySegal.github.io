---
layout: post
title: Python images downloader
tags: [python-programming-language, oop]
---
Get those images. In a smart and efficient way.

Given a plaintext file containing URLs, it will iterate over each link, filter out any non-URLs, non-image types, blank lines and etc. In this way, it ensures to be operating only on image formats such as jpg/png/etc. In case there exist a file with similar name already, the program will ask the user how it should continue.

I created a class which holds the image data:
* Output filename method.
* Image format (jpg, tiff, png, etc) method which uses the requests library to determine image format.
* overwrite method, a user choice.
* download image content using the urllib.request library, this was chosen among other methods of acquiring image content (binary copy & paste for example).

The code is [available on GitHub](https://github.com/NoySegal/ImagesDownloader).
