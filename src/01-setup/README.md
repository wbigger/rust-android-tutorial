# Setting up a development environment
There are several ways to have everything you need for this tutorial.

## With docker or a fresh new environment
The [android-rs-glue] tutorial walk you through setting the environment using a docker image or
installing everything you need from scratch.

[android-rs-glue]: https://github.com/tomaka/android-rs-glue

## With Android Studio

If you have Android Studio installed you can leverage on all the stuff
that Android Studio has already downloaded, avoiding sdk duplicates on your hard drive.

> Note: This tutorial has been tested on a mac. Everything should work fine on windows and linux,
but not tested yet. Contributes are welcomed!



- install [rustup](http://rustup.rs)
- run `rustup target add arm-linux-androideabi`, or any other target that you want to compile to
- install [gradle](https://gradle.org/install/)
- install `cargo-apk` with `cargo install cargo-apk`

> Please verify that cargo apk is v0.3.0+. If not, download the last version
directly from github with the command `cargo install --git https://github.com/tomaka/android-rs-glue cargo-apk`

Now, Open [Android Studio], go to the SDK Manager and install the following:
- SDK platforms: Android 4.3, API Level 18
- SDK Tools
   - Build Tools version 26.0.1 (for cargo-apk)
   - LLDB, CMake, NDK (for Android NDK)

> Why Android API 18? Today, Rust’s arm-linux-androideabi target is built against
that API level, and should theoretically be forwards-compatible with subsequent
Android API levels. So it picks level 18 to get the greatest Android
compatibility that Rust presently allows.

On the top of this window there is the Android SDK Location; take note of this path.

Set these two environment variables:
 - `ANDROID_HOME` to the path of the Android SDK location
 - `NDK_HOME` to the path: `$ANDROID_HOME/ndk-bundle`

[Android Studio]:https://developer.android.com/studio/index.html
