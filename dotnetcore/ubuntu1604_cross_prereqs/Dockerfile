FROM microsoft/dotnet-buildtools-prereqs:ubuntu1604_cross_prereqs_v3

RUN apt-get update \
    && echo "deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial-3.9 main" >> /etc/apt/sources.list.d/llvm.list \
    && echo "deb-src http://apt.llvm.org/xenial/ llvm-toolchain-xenial-3.9 main" >> /etc/apt/sources.list.d/llvm.list \
    && wget -O - http://apt.llvm.org/llvm-snapshot.gpg.key|apt-key add - \
    && apt-get update \
    && apt-get install -y \
        llvm-3.9 \
        clang-3.9 \
        lldb-3.9 \
        python-lldb-3.9 \
    && rm -rf /var/lib/apt/lists/*

