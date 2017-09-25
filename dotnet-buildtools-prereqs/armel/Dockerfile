FROM microsoft/dotnet-buildtools-prereqs:ubuntu-14.04-cross-0cd4667-20172211042239
MAINTAINER Hyung-Kyu Choi <hk0110.choi@samsung.com>

# Add toolchain for armel (softfp) 
# binutils-arm-linux-gnueabi
RUN apt-get update \
    && apt-get install -y \
        binutils-arm-linux-gnueabi
