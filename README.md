# sinaptika/libtorrent
Docker image for libtorrent  
From alpine: 3.6  
libtorrent x86-64:  
Docker tags:  
Latest (1.0.11), 1.0.11, 1.1.3, 1.1.4  
This image contains libtorrent x86-64.  
Libtorrent is an open source C++ library implementing the BitTorrent protocol.  
Used as base image for deluge and deluged.  

[libtorrent](http://www.libtorrent.org/)  
[Github](https://github.com/git-sinaptika/libtorrent)

Changelog:  
0.1-0.2: Build locally and on docker hub  
0.3: Strip  
0.4-0.5 Remove static library from 1.1.4 image

## Todo
- Figure out geoip and libiconv, should not be a problem on linux?
- Figure out if any gains from o3 and of course figure out autotools flags
- Figure out shared object versioning and implement in dockerfile?
- Figure out strip and make install-strip difference and find correct way?
