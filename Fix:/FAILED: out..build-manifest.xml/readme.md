Failed the first few times.

I wrote to the manifest file myself by running the python .repo script manually:
```
python3 .repo/repo/repo manifest -o - -r | grep -Ev \"proprietary_\" > out/target/product/emu64x/obj/ETC/build-manifest_intermediates/build-manifest.xml
```

Also remounted the external build-data partition:
```
cd ~
sudo mount -o remount,rw android
```

After that it Worked! and built successfully

build.log:
>>2024-11-24 21:19:39 - build_super_image.py - INFO    : Done writing image out/target/product/emu64x/super.img
>[100% 5399/5399 53m27s remaining] Create system-qemu.img now
>
>#### build completed successfully (08:55 (mm:ss)) ####
