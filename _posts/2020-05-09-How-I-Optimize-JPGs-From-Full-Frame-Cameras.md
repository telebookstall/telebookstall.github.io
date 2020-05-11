---
layout: post
title: How I Optimize JPGs From Full Frame Cameras
---

For a couple months, I wondered how I could efficiently optimize images for a blog setting, where you want a careful balance between file size and quality.

I had a couple requirements of my own:

* I must be able to optimize all images within macOS terminal, no external apps
* The images must look great on this blog, which is 1200px max width
* Each file should not exceed 1MB for any image

I eventually settled on using [ImageMagick](https://imagemagick.org/index.php), which is a popular free software capable of manipulating images. Installing it is straightforward on macOS.

```zsh
brew install imagemagick
```

I eventually settled on this specific setting:

```zsh
mogrify -resize 2400x3600\> -quality 80 -sampling-factor 4:2:0 *.JPG
```

You can run this command on terminal after cd'ing into the folder of images you want to convert. The command works for both vertical and horizontal oriented images.

There were a couple things I had to learn through trial and error:

* In order to show these images with great quality on retina screens, you have to double the dimension specified by the site. Thus, 1200 * 2 = 2400 px (horizontal) width is necessary for horizontal pics. 
* Quality 80 is good enough for a blog like this. If you go further down, I can see the blurriness of the images. If you go up from 80, the file sizes become massive. I think 80 is a great sweet spot. 
* The '>' flag is to restrict IM so that it will only shrink images to fit into the size given. Never enlarge. Considering how big JPGs come out from my Leica Q, this will shrink horizontal images to 2400x1600, and vertical images to 1600x2400. The backslash is for UNIX to recognize this special character.

Of course, this method I use is probably not perfect. However, it works great as of now, and I can hope to update this post as I keep perfecting the method.
