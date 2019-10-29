# visualization.starburst addon for Kodi

This is a [Kodi](http://kodi.tv) visualization addon.

[![Build Status](https://travis-ci.org/xbmc/visualization.starburst.svg?branch=Leia)](https://travis-ci.org/xbmc/visualization.starburst/branches)
[![Build Status](https://ci.appveyor.com/api/projects/status/github/xbmc/visualization.starburst?branch=Leia&svg=true)](https://ci.appveyor.com/project/xbmc/visualization-starburst?branch=Leia)

![screenshot](https://raw.githubusercontent.com/xbmc/visualization.starburst/Leia/visualization.starburst/resources/screenshot-01.jpg)

## Build instructions
When building the addon you have to use the correct branch depending on which version of Kodi you're building against. 
If you want to build the addon to be compatible with the latest kodi `master` commit, you need to checkout the branch with the current kodi codename.
Also make sure you follow this README from the branch in question.

### Linux

The following instructions assume you will have built Kodi already in the `kodi-build` directory 
suggested by the README.

1. `git clone --branch Leia https://github.com/xbmc/xbmc.git`
2. `git clone --branch Leia https://github.com/xbmc/visualization.starburst.git`
3. `cd visualization.starburst && mkdir build && cd build`
4. `cmake -DADDONS_TO_BUILD=visualization.starburst -DADDON_SRC_PREFIX=../.. -DCMAKE_BUILD_TYPE=Debug -DCMAKE_INSTALL_PREFIX=../../xbmc/kodi-build/addons -DPACKAGE_ZIP=1 ../../xbmc/cmake/addons`
5. `make`

The addon files will be placed in `../../xbmc/kodi-build/addons` so if you build Kodi from source and run it directly 
the addon will be available as a system addon.
