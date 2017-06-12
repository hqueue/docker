# Recovered by
# docker history --no-trunc microsoft/dotnet-buildtools-prereqs:ubuntu-14.04-cross-0cd4667-20172211042239

### Maybe following history is imported from base ubuntu 14.04 image
#3 months ago        /bin/sh -c #(nop)  CMD ["/bin/bash"] 0 B                 
#3 months ago        /bin/sh -c mkdir -p /run/systemd && echo 'docker' > /run/systemd/container 7 B                 
#3 months ago        /bin/sh -c sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list 1.9 kB              
#3 months ago        /bin/sh -c rm -rf /var/lib/apt/lists/* 0 B                 
#3 months ago        /bin/sh -c set -xe   && echo '#!/bin/sh' > /usr/sbin/policy-rc.d  && echo 'exit 101' >> /usr/sbin/policy-rc.d  && chmod +x /usr/sbin/policy-rc.d   && dpkg-divert --local --rename --add /sbin/initctl  && cp -a /usr/sbin/policy-rc.d /sbin/initctl  && sed -i 's/^exit.*/exit 0/' /sbin/initctl   && echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup   && echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean  && echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean  && echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean   && echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages   && echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes   && echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests   195 kB              
#3 months ago        /bin/sh -c #(nop) ADD file:a642bdc2d8d6e4484e4419fc938e24b03454e36f389233f2ce77fc04722da900 in / 188 MB              


FROM ubuntu:14.04

# Do we need this? It seems to be not neccesary
#RUN apt-get update \
#    && apt-get install -y \
#        git \
#        nodejs \
#        nodejs-legacy \
#        npm \
#        tar \
#        zip \
#    && rm -rf /var/lib/apt/lists/* \
#    && npm install -g azure-cli \
#    && npm cache clean

# Dependencies
RUN apt-get update \
    && apt-get install -y \
        gettext \
        libcurl4-openssl-dev \
        libicu-dev \
        liblttng-ust-dev \
        libssl-dev \
        libunwind8 \
        libunwind8-dev \
        uuid-dev \
    && rm -rf /var/lib/apt/lists/*

# Add dependencies for building cross rootfs
RUN apt-get update  \
    && apt-get install -y \
        binfmt-support  \
        cmake \
        debootstrap \
        make \
        qemu \
        qemu-user-static \
    && rm -rf /var/lib/apt/lists/*

# Add rootfs
# /bin/sh -c #(nop) ADD dir:dd0200ce8a2a337d241f4f4c0a4a9cdd1210fee6b16b51e669276bed0cbd4d1f in crossrootfs 785 MB              
