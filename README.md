# Recursive diamonds/circles 

Render recursive diamond and circle wallpaper using this GIMP Plugin.

![](previews/untitled-2_20240913145542629.png)

![](previews/untitled-2_20240913145943292.png)


## Directory to put Binaries (They do NOT go in the normal plugins folder)

**Windows**

 C:\Users\(USERNAME)\AppData\Local\gegl-0.4\plug-ins

 **Linux**

`~/.local/share/gegl-0.4/plug-ins`

 **Linux (Flatpak includes Chromebook)**

`~/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins`

Then Restart Gimp and go to GEGL Operations and look for "Recursive Diamonds/Circles" in the drop down list,
Gimp 2.99.16+ users will find the filter in filters>render>fun. 2.10 users will only see it in the GEGL operations drop down list.


## Compiling and Installing

As of August 2024 all my plugins can be compiled by running build_plugin_linux/windows.sh and even long before that there was build_linux.sh. Said scripts that these plugins ship with runs the same meson ninja commands as listed below.

### Linux

To compile and install you will need the GEGL header files (`libgegl-dev` on
Debian based distributions or `gegl` on Arch Linux) and meson (`meson` on
most distributions).

```bash
meson setup --buildtype=release build
ninja -C build

```

### Windows

The easiest way to compile this project on Windows is by using msys2.  Download
and install it from here: https://www.msys2.org/

Open a msys2 terminal with `C:\msys64\mingw64.exe`.  Run the following to
install required build dependencies:

```bash
pacman --noconfirm -S base-devel mingw-w64-x86_64-toolchain mingw-w64-x86_64-meson mingw-w64-x86_64-gegl
```

Then build the same way you would on Linux:

```bash
meson setup --buildtype=release build
ninja -C build
```


### More previews of this based plugin

![](previews/untitled-1_20240913150414037.png)

![](previews/untitled-1_20240913150243840.png)

