# Alpine Term

This is a terminal emulator and a Linux environment application using
the [QEMU](https://qemu.org) to run the [Alpine Linux](https://alpinelinux.org)
distribution.

*Inspired by [Termux](https://github.com/termux/termux-app) and
[UserLAnd](https://github.com/CypherpunkArmory/UserLAnd) applications.*

<p align="center"><img src="help-page/img/demo_anim.gif" width="60%"></p>

**Disclaimer**: by installing this software, you are agreeing to use it
on your own risk. Alpine Term comes with disk image file containing the
software developed by third-parties. [Author](https://github.com/xeffyr)
is not responsible for any damage that may affect your device or data.

## System requirements

In general, it should work on any high-end device which met the following
requirements:

 - Android 7.0 or higher.
 - At least 1 GB of space on the internal storage.

## Extra packages

Check the https://github.com/xeffyr/alpine-extra-ports for some additional
packages which may not be available in Alpine official repositories.

## Consider this before opening a new [issue](https://github.com/xeffyr/alpine-term/issues)

Bugs:

 - Application is based on [Termux](https://github.com/termux/termux-app/)
   project and shares many code parts. Therefore it can share same bugs too.
 
 - Operating system ([Alpine Linux](https://alpinelinux.org/)) is configured
   to use edge repository where software is at latest available version which
   may be unstable. Do not report OS bugs to [this](https://github.com/xeffyr/alpine-term)
   repository !

 - Alpine Linux uses [Musl](https://www.musl-libc.org/) libc which is not
   compatible with GNU libc. Certian programs will not work here - do not
   complain about that.

Feature requests:

 - Application will never support Android OS versions below 7.0.

 - Application is designed to be minimal. It is mostly a text-based interface
   to QEMU. If requested feature goes beyond that concept, it may be ignored.

 - Application is designed to run only Alpine Linux. Requests for support of
   Ubuntu, Debian, Arch, whatever else will be ignored.

 - Emulator configuration is designed to be immutable and determined at compile-time
   of the application. You can use QEMU monitor for some runtime tweaks. For
   example to add a custom HDD image, create snapshot, backup, etc...

 - Application is configured to place OS image into private directory on internal
   storage. This is done due to stability and privacy concerns.

 - External and shared storage support is limited. Emulator is configured only to use
   application private directory located in user space, typically:
   ```
   /storage/emulated/0/Android/data/alpine.term/files
   ```
   Requests for full external/shared storage support will be ignored.

 - KVM support will never be enabled.

## Credits

Alpine Term relies on the source code of the following projects:

 - [Termux](https://github.com/termux/termux-app)
 - [QEMU](https://qemu.org)
 - [Socat](http://www.dest-unreach.org/socat/)
