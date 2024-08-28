 FROM ubuntu:24.04
 RUN apt-get update && \
     apt-get install -y \
            autoconf \
            automake \
            autotools-dev \
            curl \
            libmpc-dev \
            libmpfr-dev \
            libgmp-dev \
            libusb-1.0-0-dev \
            gawk \
            build-essential \
            bison \
            flex \
            texinfo \
            gperf \
            libtool \
            patchutils \
            bc \
            zlib1g-dev \
            device-tree-compiler \
            pkg-config \
            libexpat-dev \
            wget \
            cpio \
            python3 \
            unzip \
            rsync \
            libncurses-dev \
            sudo \
            git && \
    apt-get clean ; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/* ; \
    groupadd wheel -g 998; \
    userdel ubuntu; \
    rm -rf /home/ubuntu; \
    useradd cva6-sdk -u 1000 -g wheel; \
    mkdir -p /home/cva6-sdk; \
    chown cva6-sdk:wheel /home/cva6-sdk; \
    echo "\n%wheel ALL=(ALL:ALL) NOPASSWD: ALL" >> /etc/sudoers
  USER cva6-sdk:wheel
