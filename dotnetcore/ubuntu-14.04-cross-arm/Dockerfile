FROM hqueue/dotnetcore:ubuntu-14.04-cross-base
MAINTAINER Hyung-Kyu Choi <hk0110.choi@samsung.com>

# Add toolchain for arm (hardfp) 
# binutils-arm-linux-gnueabihf and clang 3.9
RUN apt-get update \
    && apt-get install -y \
        binutils-arm-linux-gnueabihf \
        wget \
    && echo "deb http://apt.llvm.org/trusty/ llvm-toolchain-trusty-3.9 main" >> /etc/apt/sources.list.d/llvm.list \
    && echo "deb-src http://apt.llvm.org/trusty/ llvm-toolchain-trusty-3.9 main" >> /etc/apt/sources.list.d/llvm.list \
    && wget -O - http://apt.llvm.org/llvm-snapshot.gpg.key | apt-key add - \
    && apt-get update \
    && apt-get install -y \
        llvm-3.9 \
        clang-3.9 \
        lldb-3.9 \
    && rm -rf /var/lib/apt/lists/*

# Add rootfs
# /bin/sh -c #(nop) ADD dir:dd0200ce8a2a337d241f4f4c0a4a9cdd1210fee6b16b51e669276bed0cbd4d1f in crossrootfs 785 MB              
