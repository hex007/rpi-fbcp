Raspberry Pi VSynced Framebuffer Copy
=============================
This program used for copy primary framebuffer to secondary framebuffer (eg. FBTFT). It requires lastest raspberry pi firmware (> 2013-07-11) to work properly.

I changed the original while loop into a callback function on fb0 vsync and added a pause() instead. This makes sure every frame on fb0 gets copied to fb1 right after it gets refreshed at the cost of a slight increase of CPU usage (~1% @30pfs).

Build
-----
```
 $ mkdir build
 $ cd build
 $ cmake ..
 $ make 
```
