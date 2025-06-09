# crkbd_rev1_layout

## Setup

Follow https://docs.qmk.fm/newbs_getting_started and make sure that the following command works:
```
qmk compile -kb crkbd/rev1 -km default -e CONVERT_TO=rp2040_ce
```

## Create new keymap
```
qmk config user.keyboard=crkbd/rev1
qmk config user.keymap=tswr
qmk new-keymap
```

Replace created files with the files from this repository

## Build

```
qmk clean
qmk compile
```

## Flash

For both splits enter the bootloader and
```
sudo mount -o uid=1000,gid=1000 /dev/sdb1 /mnt/rp2040
cp ~/qmk_firmware/crkbd_rev1_tswr_rp2040_ce.uf2 /mnt/rp2040/
sudo umount /mnt/rp2040
```
