Ray Tracing in one Weekend in CUDA
==================================

This is yet another _Ray Tracing in One Weekend_ clone, but this time using CUDA instead of C++.

By Roger Allen
May, 2018

Background
----------

Peter Shirley has written a few ebooks about Ray Tracing.  You can find out more at http://in1weekend.blogspot.com/2016/01/ray-tracing-in-one-weekend.html  Note that as of April, 2018 the books are *pay what you wish* and 50% of the proceeds go towards not-fo-profit programming education organizations.  It's also available for $3 on Amazon as a Kindle download.

Before coding this in CUDA, I recommend that you code this in C++, first.  You should understand the concepts presented in a serial language first, then translate this knowledge to CUDA.  In fact, since CUDA uses C++, much of your code can be reused.

The canonical C++ code from Peter Shirley is at https://github.com/petershirley/raytracinginoneweekend.  I am basing this on https://github.com/pfranz/raytracinginoneweekend which has each chapter as a separate git branch.  This is very handy for checking out the code at each chapter.

Chapter 1
---------

This introduces the basic kernel launch mechanism & host/device memory management.  We are just creating an image on the GPU device and cudaMallocmanaged allows for sharing the framebuffer and automatically copying that buffer to & from the device.

I also added a timer to see how long it takes the GPU to do rendering.
