FreeImage-OSX
=============

I've modified the original Makefile.osx from FreeImage 3.15.4 in order to compile on OS X Mountain Lion with Clang and libc++.

You will also need to add *#include &lt;string.h&gt;* in Source/OpenEXR/IlmImf/ImfAutoArray.h. 

With the above modifications compiling FreeImage on ML with Xcode Command Line Tools installed is as simple as:

*make*

*sudo make install*

The above will install FreeImage in /usr/local.

Compiling and linking with FreeImage can be achieved with:

*clang++ -stdlib=libc++ your_program_name.cpp -lfreeimage*

These modifications are provided under the same terms as FreeImage 3.15.4.
