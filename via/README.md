# VIA support for Breeze

## Workaround to get it going now:

* Download `afternoonlabs_breeze_rev1_via.hex` from this repo and flash it to your board using the using QMK Toolbox: https://github.com/qmk/qmk_toolbox
* Download and install the VIA configurator UI: https://github.com/the-via/releases/releases
* Download the `breeze.json` from this directory and save it some easily accessible place on your file system.
* In the VIA tool, click on the "Settings" tab:
![Settings Tab](https://i.imgur.com/6Gseg6Q.png)
* Enable "Show Design Tab":
![Show Design Tab](https://i.imgur.com/2d8rrwL.png)
* In the Design tab, use "Load" button for "Load Draft Definition":
![Load Draft Definition](https://imgur.com/5c8jwh1.png)
* You should now be able to use the "Configure" tab as per normal.  Changes should be live as you make them.  If you have to reload the configurator later, you will need to reload the draft definition.

## Pending changes:

VIA support requires a change to QMK to enable VIA for the board firmware and a change to the VIA configurator tool.  Pull requests for both changes are pending but there is a suitable manual override in the meantime:

* QMK changes: qmk/qmk_firmware#12247
* VIA changes: the-via/keyboards#627

## Known Problems / Limitations

* Mouse keys don't seem to work properly.  You can map them and the configuration sticks but the internal mapping is messed up somehow (mouse up produces mouse left, mouse left does mouse button1 etc.)
* Everything else seems to work, including macros.
