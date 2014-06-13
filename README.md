
# JpegOptimImage 0.1.0

Optimize jpegs with jpegoptim

## Installation

### Install jpegoptim

I couldn't find a repository for it but it wasn't hard to compile. I've only done so on a Debian system but the below are the steps I used:
* apt-get install libjpeg-dev
* Download the latest source from [kokkonen.net](http://www.kokkonen.net/tjko/projects.html)
* tar zxvf jpegoptim-1.4.1.tgz
* cd jpegoptim-1.4.1
* ./configure
* make 
* make install

### Install this ProcessWire module

The [usual methods](http://modules.processwire.com/install-uninstall/) apply.

## Usage

Resized images are automagically optimized:

`echo $page->image->size(50, 50)->url; // no need to call optimize

If you don't need to resize the image you can call optimize like in the below:

`echo $page->image->optimize()->url;`
