#Maintainer info@sinaptika.net
#libtorrent http://www.rasterbar.com/products/libtorrent/
#libtorrent image
FROM alpine:3.6

ENV \
 LIBTORRENT_VERSION="1.0.11" \
 _LIBTORRENT_VERSION="1_0_11"

WORKDIR \
 /root

RUN \
#Libtorrent
 apk add --no-cache --virtual .build_libtorrent \
  wget ca-certificates alpine-sdk boost-dev libressl-dev python2-dev && \
 cd /root && \
 wget -qO-\
  https://github.com/arvidn/libtorrent/releases/download/libtorrent-${_LIBTORRENT_VERSION}/libtorrent-rasterbar-${LIBTORRENT_VERSION}.tar.gz | \
  tar xvz && \
 cd libtorrent-rasterbar-${LIBTORRENT_VERSION} && \
 ./configure \
  --build=$CBUILD \
  --host=$CHOST \
  --prefix=/usr \
  --enable-python-binding \
  --with-boost-system=boost_system \
  --enable-debug=no \
  --disable-debug \
  --quiet && \
 make && \
 make install-strip && \
 #rm -rf /usr/lib/libtorrent-rasterbar.a && \
 strip /usr/lib/python2.7/site-packages/libtorrent.so && \
 strip /usr/lib/libtorrent-rasterbar.so && \
 rm -rf libtorrent-rasterbar-${LIBTORRENT_VERSION} && \
 apk del .build_libtorrent && \
 apk add --no-cache --virtual .runtime_libtorrent \
  boost-python boost-system libgcc libstdc++ python2

LABEL \
 net.sinaptika.maintainer="info@sinaptika.net" \
 net.sinaptika.name="libtorrent" \
 net.sinaptika.branch="master" \
 net.sinaptika.from="alpine:3.6" \
 c_software_name="libtorrent" \
 c_software_url="http://www.rasterbar.com/products/libtorrent/" \
 image.version="0.4" \
 date.version="5.8.2017" \
 web_interface="false" \
 web_interface_port="false" \
 exposed_ports="false" \
 docker_volumes="false"
