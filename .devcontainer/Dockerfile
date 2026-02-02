FROM mcr.microsoft.com/devcontainers/cpp:ubuntu


# create a user matching host UID and GID

RUN apt-get update && \
    #add-apt-repository -y universe && \
    apt-get update && \
    apt-get install -y build-essential gcc-arm-none-eabi libnewlib-arm-none-eabi minicom

RUN cd /opt &&\
    git clone -b master https://github.com/raspberrypi/pico-sdk.git && \
    cd pico-sdk && \
    git submodule update --init

ENV PICO_SDK_PATH=/opt/pico-sdk
RUN echo 'alias pmake="cp /opt/pico-sdk/external/pico_sdk_import.cmake ./ && cp /opt/pico-sdk/external/pico_sdk_import.cmake ."' >> /etc/bash.bashrc
RUN git config --global --add safe.directory "*" && git config --global init.defaultBranch main
