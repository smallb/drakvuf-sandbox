ARG IMAGE
FROM $IMAGE

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y \
    wget python3.7 python3.7-venv python3-pip dh-virtualenv debhelper devscripts \
    libpixman-1-0 libpng16-16 libfdt1 libglib2.0-dev libjson-c3 libyajl2 libaio1 && \
    python3.7 -m pip install pip

RUN wget -O drakvuf.deb https://github.com/tklengyel/drakvuf-builds/releases/download/20200317014821-a1ef03c/drakvuf-bundle-0.7-a1ef03c-generic.deb && \
    dpkg -i drakvuf.deb

COPY drakrun /build
WORKDIR /build
