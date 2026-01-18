FROM mcr.microsoft.com/devcontainers/cpp:ubuntu


RUN apt-get update && \
    #add-apt-repository -y universe && \
    apt-get update && \
    apt-get install -y gcc-arm-none-eabi libnewlib-arm-none-eabi minicom

RUN cd /opt &&\
    git clone -b master https://github.com/raspberrypi/pico-sdk.git && \
    cd pico-sdk && \
    git submodule update --init

ENV PICO_SDK_PATH=/opt/pico-sdk
