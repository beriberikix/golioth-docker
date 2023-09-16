# golioth-docker

Build command:

```
docker build -t golioth-zephyr-arm:v3.4.0-0.16.1 -f Dockerfile.zephyr .
```

Defaults to Zephyr v3.4.0 and arm SDK v0.16.1.

Target different toolchains:

```
docker build -t golioth-zephyr-x86:v3.4.0-0.16.1 --build-arg="ZEPHYR_SDK_TOOLCHAIN=-t x86_64-zephyr-elf" -f Dockerfile.zephyr .
```

Target different vendors:
```
docker build -t golioth-zephyr-espressif:v3.4.0-0.16.1 --build-arg="ZEPHYR_SDK_TOOLCHAIN=-t  xtensa-espressif_esp32s2_zephyr-elf -t xtensa-espressif_esp32s3_zephyr-elf -t xtensa-espressif_esp32_zephyr-elf" -f Dockerfile.zephyr .
```

Example Docker image files on disk since last README update:

* golioth-zephyr-arm:v3.4.0-0.16.1       => 1396 MB
* golioth-zephyr-x86:v3.4.0-0.16.1       => 731  MB
* golioth-zephyr-espressif:v3.4.0-0.16.1 => 1035 MB