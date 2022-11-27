## Debian Packaing

* Simple and useful example here: https://wiki.debian.org/Packaging/Intro
* And this doc for setting up a local repo for debian packages: https://rpmdeb.com/devops-articles/how-to-create-local-debian-repository/
* These are docker images for having a ready debian build os: https://github.com/tsaarni/docker-deb-builder
* This is my custom docker image based on ubuntu@22.04 to build qt application packaging:
```docker
ROM ubuntu:22.04

ARG DEBIAN_FRONTEND=noninteractive

RUN set -ex \
    && sed -i -- 's/# deb-src/deb-src/g' /etc/apt/sources.list \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
               build-essential \
               cdbs \
               devscripts \
               equivs \
               fakeroot \
    && apt-get clean \
    && rm -rf /tmp/* /var/tmp/*
RUN apt-get install -y meson \
wget nano debmake cmake python3-debian \
curl git \
qtbase5-dev qtbase5-dev-tools qt5-qmake \
pulseaudio \
qtquickcontrols2-5-dev qtdeclarative5-dev qml-module-qtquick-controls \
qml-module-qtquick-controls2 qml-module-qtquick-dialogs \
qml-module-qt-labs-platform qtdeclarative5-private-dev \
qtmultimedia5-dev qml-module-qtmultimedia qml-module-qtgraphicaleffects qml-module-qtquick-extras \
libevent-dev libevent-2.1-7 \
libnice10 libnice-dev \
liblmdb0 liblmdb-dev \
zlib1g zlib1g-dev \
libcurlpp-dev libcurl4 \
nlohmann-json3-dev \
cmark libcmark-dev \
libnice10 libnice-dev \
libqt5svg5-dev \
libpulse-dev \
doctest-dev
ADD http://ftp.de.debian.org/debian/pool/main/d/dh-cmake/dh-cmake_0.6.1_all.deb /home/deb-files/
RUN dpkg -i /home/deb-files/dh-cmake_0.6.1_all.deb && rm /home/deb-files -rf
```

Run to build image:
```bash
docker build -t docker-deb-builder:22.04 -f Dockerfile-ubuntu-22.04 .
```

Running the container:
```bash
docker run -it --volume deb-packaging-vol:/root/ --name deb-pkg docker-deb-builder:22.04
```

* This is debian package source files of `nheko`: https://salsa.debian.org/matrix-team/nheko/-/tree/master/debian

