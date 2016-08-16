Raspberry Pi Framebuffer Copy
=============================
This program used for copy primary framebuffer to secondary framebuffer (eg. FBTFT). It require lastest raspberry pi firmware (> 2013-07-11) to working properly.

I changed the while loop into a callback function on fb0 vsync and added a pause() instead. This makes sure every frame on fb0 gets copied to fb1 right after it got refreshed.

Build
-----
```
 $ mkdir build
 $ cd build
 $ cmake ..
 $ make 
```
