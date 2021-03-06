AtomicParsley
-------------

AtomicParsley is a lightweight command line program for reading, parsing and setting metadata into MPEG-4 files, in particular, iTunes-style metadata. It is useful to edit tags for movies,tv-shows and music-video's (.m4v), audio (.m4a) and ringtones (.m4r).

The original code v0.9.0, which was last updated in 2006 is located here: [atomicparsley.sf.net](http://atomicparsley.sourceforge.net).

For my project, I have forked the latest version I could find, dated 2014, from [Dan Drusch](https://github.com/DanDrusch/atomicparsley.git).
In 2019 I have manually merged new updates from sourceforge.

My instructions below are for OSX only; sorry.

## Build using Xcode

I am now building using Xcode v9.4.1.

Under the Releases tab, you find a binary executable, signed with my developer account.
To run it, allow "App Store and identified developers" in the "Security & Privacy" control panel.


## Legacy Setup the build environment:

Now that I'm using Xcode, the instructions below for a command-line build are not used.

I keep them here for reference- to show how this sourcec-code archive was created.

### 1.Install the OSX C-compiler
 * Logon to https://developer.apple.com/downloads/
 * Under "Developer Tools" download Xcode
 * Under "Developer Tools" download Xcode command line tools (matching for your OS)
 * Install Xcode
 * Install Xcode command line tools

### 2.Install autoconf
```
  cd ~/Desktop
  curl -OL http://ftpmirror.gnu.org/autoconf/autoconf-2.68.tar.gz
  tar xzf autoconf-2.68.tar.gz
  cd autoconf-2.68
  sudo make install
```
### 3.Install automake
```
  cd ~/Desktop
  curl -OL http://ftpmirror.gnu.org/automake/automake-1.11.tar.gz
  tar xzf automake-1.11.tar.gz
  cd automake-1.11
  ./configure --prefix=/usr/local
  sudo make install
```
### 3.Install zlib
```
  cd ~/Desktop
  mkdir zlib
  cd zlib
  curl -OL http://zlib.net/zlib-1.2.8.tar.gz
  tar xzf zlib-1.2.8.tar.gz
  cd zlib-1.2.8
  ./configure --prefix=/usr/local
  sudo make install
  find /usr/lib -name "*libz*"
```
### 3.Check out the code
```
   mkdir ~/Github
   cd ~/Github
   git clone https://github.com/bergertom/atomicparsley.git
   cd atomicparsley
```
   
## Compiling the code
```
This will generate the AtomicParsley executeable.
   cd ~/Github/atomicparsley
  ./autogen.sh
  ./configure --disable-universal
   make
```
I am just using Xcode ...
  

