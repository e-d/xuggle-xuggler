# Xuggler

## What's different in this fork?

Time has been spent in trying to successfully build the original
GPL licensed version of the source code along with an LGPL
variant. This trial-and-error build knowledge has been put into
the [build-help.txt](https://github.com/e-d/xuggle-xuggler/blob/master/build-help.txt) file. 

To view a formatted version of build-help.txt (with links) you can [click here](https://docs.google.com/document/d/1mjlI2jAGKK3_W4KIBjpUfM3F_SJjUkZhQJuwtIBn_7I/pub).

This file contains the steps taken to successfully build the latest 5.5 source code for:
- Windows (32-bit) (via cross-compiling on Linux)
- Windows (64-bit) (via cross-compiling on Linux)
- Linux (32-bit)
- Linux (64-bit)

Changes to help build the LGPL version of the binaries were done
in the [jawallace/xuggle-xuggler](https://github.com/jawallace/xuggle-xuggler) fork.


## README from [xuggle/xuggle-xuggler](https://github.com/artclarke/xuggle-xuggler) base project

### Welcome to Xuggle-Xuggler-Main (a.k.a. Xuggler)

http://www.xuggle.com/xuggler

#### Licensing

Xuggler is licensed under the Lesser GNU Public License, but if
compiled with a GPL version of FFmpeg, then Xuggler assumes
the GPL license (as required by FFmpeg).

See the COPYING file for our license, along with the amending
COPYING.LESSER file.

For the license used in libraries in the 'captive' directory,
see the captive directory.

#### What is Xuggler?

Xuggler is a Java library that allows you to decode and
encode a variety of media file formats directly from Java.

It is built on top of the FFMPEG (http://ffmpeg.org/), but
is designed with the following goals:
- Ease of Use: Provide the power of FFMPEG with an easier learning curve for developers.
- Safety: Run natively inside a Virtual Machines (e.g. Java) and servers, but minimize the odds of incorrect coding of native FFMPEG code causing crashes.
- Portability: Write portable code that should run most places where FFMPEG can run.

#### What languages are supported?

Today Xuggler works under Java

People can also use the C++ api directly, but bear in mind three caveats:
- You must explicitly release all references you create to objects
  with ->release() calls; every make() or get...() method returns
  a reference.  A template class called com.xuggle.ferry.RefPointer
  is provided that can do a lot of the release()ing for you, but
  it's no substitute for care on your part.

- Our current build system relies on autoconf and g++, so
  linking this C++ library on Windows can be difficult if you're
  using Microsoft's Visual C++ compiler.

#### How to use Xuggle?

You must first build and install Xuggle for the operating
system you will use it on.  Unlike most Java libraries,
Xuggle has a native (e.g. Windows DLL or Linux shared library)
component that must be installed with it.

See the INSTALL file for instructions.

Once installed, just make sure your Java program references
xuggle-xuggler.jar, and you should be able to use the API.

#### Where can I find documentation?

Visit http://www.xuggle.com/xuggler/doc

or build the documentaiton yourself:
  ant doc
and then open up
  doc/java/api/index.html (the Java docs).
  doc/cpp/api/html/index.html (the C++ docs if you have Doxygen installed).

Currently the Java docs are auto-generated from the C++ docs and
there are quite a few bugs with that.  If you're not getting
what you need from the Java docs, then please, check out the C++ docs.

#### Where can I find out more?

Visit:
http://www.xuggle.com/xuggler

