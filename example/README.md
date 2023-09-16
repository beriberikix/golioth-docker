Build Basics example for RT1024

```
docker build -t goliothbasics:rt1024 .
```

Copy `build` to local machine (use running container)

```
docker cp 7848d9401219:zephyrproject/modules/lib/golioth-firmware-sdk/build/zephyr
```