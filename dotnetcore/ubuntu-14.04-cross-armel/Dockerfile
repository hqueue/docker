FROM hqueue/dotnetcore:ubuntu-14.04-cross-arm
MAINTAINER Hyung-Kyu Choi <hk0110.choi@samsung.com>

# Add toolchain for armel (softfp) 
# binutils-arm-linux-gnueabi
RUN apt-get update \
    && apt-get install -y \
        binutils-arm-linux-gnueabi

# Add rootfs
# /bin/sh -c #(nop) ADD dir:dd0200ce8a2a337d241f4f4c0a4a9cdd1210fee6b16b51e669276bed0cbd4d1f in crossrootfs 785 MB              
