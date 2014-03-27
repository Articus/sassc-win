# sassc for Visual Studio

Visual Studio 2012 solution for building [sassc](https://github.com/hcatlin/sassc) - awesome command line utility for compiling SASS to CSS.

## About

Compiling *.scss files on Windows is rather painful process. You have to either install Ruby and use [official gem](http://sass-lang.com/install) or install Node.js and use [SASS package](https://github.com/andrew/node-sass). 

Thankfully there is nice simple open source Linix command utility to do the job - [sassc](https://github.com/hcatlin/sassc). Sadly I have not found any compiled binaries of it for Windows and decided to do that myself. 

I already had VS 2012 installed so the choice of compiler was obvious. Compilation required only adding [getopt implentation for Windows](http://www.codeproject.com/Articles/157001/Full-getopt-Port-for-Unicode-and-Multibyte-Microso) and few cosmetic changes of sassc.c to make it work with getopt substitute and make VS C-compiler happy. The code of [libsass](https://github.com/hcatlin/libsass) is intact. So hopefully it would be easy update the solution to new version of libsass and sassc.


## Discalimer

The compiled executable works fine for me on Windows 8 and Windows 7, but as usual no guarantees that it will work on your system :) Feel free to build the solution by yourself and report if there are any license or technical issues. Hope I have not violated any license terms with this repository.