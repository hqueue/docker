FROM hqueue/dotnet-buildtools-prereqs:ubuntu-14.04-cross-0cd4667-20172211042239-armel
MAINTAINER Hyung-Kyu Choi <hk0110.choi@samsung.com>

# Add armel rootfs of Tizen 4.0 for cross building coreclr and corefx
ADD ./rootfs.armel.tizen.build.20170925.tar.gz /crossrootfs
ADD ./rootfs.armel.tizen.test.20170925.tar.gz /crossrootfs
