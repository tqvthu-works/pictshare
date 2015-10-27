# PictShare
PictShare is an open source image hosting service with a simple resizing API

## Why would I want to host my own images?
If you own a server (even an home server) you can host your own PictShare instance so you have full control over your content and can delete images hasslefree.

## Features
- Uploads without logins or validation (that's a good thing, right?)
- Simple API to upload any image from remote servers to your instance via URL or base64 encoded image
- 100% file based - no database needed
- PictShare removes all exif data so you can upload photos from your phone and all GPS tags and camera model info get wiped
- Builtin and simple resizing and caching
- Duplicates don't take up space. If the exact same images is uploaded twice, the second upload will link to the first

## What's that about resizing?
Lets's say you have uploaded this image: ```https://www.pictshare.net/b260e36b60.jpg``` but you want to use it as your avatar in some forum that only allows 100x100 pixel images.
Instead of editing it yourself you just use ```https://www.pictshare.net/100x100/b260e36b60.jpg```

Just by editing the URL the image gets resized and the resized version gets cached to the disk so it loads much faster.

## Security and privacy
- By hosting your own images you can delete them any time you want
- You can enable or disable upload logging. Don't want to know who uploaded stuff? Just change the setting in index.php
- No exif data is stored on the server, all jpegs get cleaned on upload

## Requirements
- Apache Webserver with PHP (Apache because of the included .htaccess files)
- PHP 5 GD library
- Some hostname or subdomain. Site might get messed up if it's not stored in the root directory of the webserver

## Coming soon
- Restricted uploads so you can control who may upload on your instance