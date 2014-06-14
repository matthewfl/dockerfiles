FROM matthewfl/archlinux-devel
MAINTAINER Matthew Francis-Landau <matthew@matthewfl.com>

RUN packer --noconfirm -S imake boost bison flex snappy curl libtorrent-rasterbar intel-tbb protobuf

RUN cd /opt && git clone git://github.com/matthewfl/ilang.git
RUN cd /opt/ilang && make submodule
RUN cd /opt/ilang && make
RUN ln -s /opt/ilang/i /usr/bin