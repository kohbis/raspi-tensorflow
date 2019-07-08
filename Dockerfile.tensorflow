FROM tensorflow/tensorflow:nightly-devel

ENV LANG "C.UTF-8"

RUN apt-get update -y
RUN apt-get install -y --no-install-recommends \
        crossbuild-essential-armhf \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

RUN /tensorflow/tensorflow/lite/tools/make/download_dependencies.sh
RUN /tensorflow/tensorflow/lite/tools/make/build_rpi_lib.sh
