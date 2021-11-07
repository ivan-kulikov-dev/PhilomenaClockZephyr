
## Initialize workspace (west init)
```
cd aphilomena-clock-os/app
west init
```
## Update modules (west update)
```
west update
```
## Export Zephyr CMake package (west zephyr-export)
```
west zephyr-export
```

## Build and flash
```
west build -b esp32
west flash
minicom --device /dev/ttyACM0
```
