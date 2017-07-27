# Verify the installation
To test the installation, you can use virtually any of your Rust project.

> Current limitation: the project has to contain a *single bin* target and
no lib targets.

To keep things simple, you can use this [sample application], that it is just
a new project with a console log output.

In the root folder of this project run:

`cargo apk build`

If everything is ok, plug your Android device to your computer and install
the application using:

`cargo apk install`

Now, show the Android log and filter our output:

`adb logcat | grep RustAndroidGlueStdouterr`

Open the application in your Android device. You should see a black screen and
a log in the console.


[sample application]: https://github.com/wbigger/rust-android-tutorial
