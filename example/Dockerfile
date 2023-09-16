FROM golioth-zephyr-arm:v3.4.0-0.16.1 as build

RUN \
  mkdir zephyrproject && cd zephyrproject \
  && west init -m https://github.com/golioth/golioth-firmware-sdk.git --mf west-zephyr.yml \
  && west update --narrow -o=--depth=1 \
  && cd modules/lib/golioth-firmware-sdk && git submodule update --init --recursive

RUN \
  cd zephyrproject/modules/lib/golioth-firmware-sdk \
  && west build -b mimxrt1024_evk examples/zephyr/golioth_basics