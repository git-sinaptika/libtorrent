# sinaptika/libtorrent
[Github](https://github.com/git-sinaptika/libtorrent)  
Docker image for libtorrent-rasterbar:  
From alpine: 3.7  

[libtorrent-rasterbar](http://www.libtorrent.org/)  
Libtorrent is an open source C++ library implementing the BitTorrent protocol.  
Both static and dynamic libraries are included.  

Docker tags:  
Latest (1.1.5), 1.0.11, 1.1.3,1.1.5, dev  

Used for multistage builds for:
[deluge](https://hub.docker.com/r/sinaptika/deluge/) and [deluged](https://hub.docker.com/r/sinaptika/deluged/).  

Changelog:  
0.1-0.2: Build locally and on docker hub  
0.3: Strip  
0.4 Unify branches and use dir structure for tags, also added 1.1.2  
0.5 Prepare for use in multi-stage builds on docker hub, add dev tag,  
remove static from docker hub automated builds, added comments to enable  
static in dockerfile.  
0.6 Syntax changes  
0.7 Updated to Alpine 3.7
0.8 Removed old versions and images based on Alpine 3.6

## Todo
- ~~Figure out geoip and libiconv, should not be a problem on linux?~~
- ~~Figure out if any gains from o3 and of course figure out autotools flags~~
- ~~Figure out shared object versioning and implement in dockerfile?~~
- ~~Figure out strip and make install-strip difference and find correct way?~~
  - ~~python-bindings are still not striped?~~
