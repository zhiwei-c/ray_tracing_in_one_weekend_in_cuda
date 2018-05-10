Ray Tracing in One Weekend in CUDA
==================================

***WORK IN PROGRESS***

***Not Done Yet***


This is yet another _Ray Tracing in One Weekend_ clone, but this time using CUDA instead of C++.  CUDA can be used to speed up the code.  For example, on my machine, the C++ code renders the test image in 80 seconds.  The CUDA accelerated code renders the image in about 8.

By Roger Allen
May, 2018

Background
----------

Peter Shirley has written a few ebooks about Ray Tracing.  You can find out more at http://in1weekend.blogspot.com/2016/01/ray-tracing-in-one-weekend.html  Note that as of April, 2018 the books are *pay what you wish* and 50% of the proceeds go towards not-for-profit programming education organizations.  They are also available for $3 each on Amazon as a Kindle download.

This repository contains code for converting the first Ray Tracer ebook from C++ to CUDA.

Before coding this in CUDA, I recommend that you code this in C++, first.  You should understand the concepts presented in a serial language well, then translate this knowledge to CUDA.  In fact, since CUDA uses C++, much of your code can be reused.

The canonical C++ code from Peter Shirley is at https://github.com/petershirley/raytracinginoneweekend.  I am basing this on https://github.com/pfranz/raytracinginoneweekend which has each chapter as a separate git branch.  This is very handy for checking out the code at each chapter.

Chapter List
------------

Here are links to the git branch for each Chapter.  If you look at the README.md you'll see some hints about what needed to be done.  See the Makefile for the standard targets.  Note that you'll want to adjust the GENCODE_FLAGS in the CUDA Makefiles for your specific graphics card architecture.

The master branch has the code as Peter Shirley presented it in C++.  I added a Makefile so you can `make out.jpg` and compare the runtime to CUDA.

* [Chapter 1 - Basic Output](https://github.com/rogerallen/raytracinginoneweekend/tree/ch01_output_cuda)
* [Chapter 2 - Vectors](https://github.com/rogerallen/raytracinginoneweekend/tree/ch02_vec3_cuda)
* [Chapter 3 - Rays](https://github.com/rogerallen/raytracinginoneweekend/tree/ch03_rays_cuda)
* [Chapter 4 - Spheres](https://github.com/rogerallen/raytracinginoneweekend/tree/ch04_sphere_cuda)
* [Chapter 5 - Normals](https://github.com/rogerallen/raytracinginoneweekend/tree/ch05_normals_cuda)
* [Chapter 6 - Antialiasing](https://github.com/rogerallen/raytracinginoneweekend/tree/ch06_antialiasing_cuda)
* [Chapter 7 - Diffuse](https://github.com/rogerallen/raytracinginoneweekend/tree/ch07_diffuse_cuda)
* [Chapter 8 - Metal](https://github.com/rogerallen/raytracinginoneweekend/tree/ch08_metal_cuda)
* [Chapter 9 - Dielectrics](https://github.com/rogerallen/raytracinginoneweekend/tree/ch09_dielectrics_cuda)
* [Chapter 10 - Camera](https://github.com/rogerallen/raytracinginoneweekend/tree/ch10_camera_cuda)
* [Chapter 11 - Defocus Blur](https://github.com/rogerallen/raytracinginoneweekend/tree/ch11_defocus_blur_cuda)
* [Chapter 12 - Where Next](https://github.com/rogerallen/raytracinginoneweekend/tree/ch12_where_next_cuda)

Colophon
--------

Basic process (after Chapter 3) was:

```
# checkout original code & create a cuda branch
git checkout origin/chyy_yyy
git checkout chyy_yyy
git branch -m chyy_yyy_cuda
git mv main.cc main.cu
<checkin>
# grab previous chapters code as a starting point
cp chapterxx/* .
# edit & fix code
# checkin code
# save current code for next chapter
mkdir chapteryy
cp * chapteryy
```
