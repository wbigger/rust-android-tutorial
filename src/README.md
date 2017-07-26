# Introduction

> Create your Android applications with [Rust]!

[Rust]: https://www.rust-lang.org/en-US/

Looking at the Google Playstore top 1000 apps, the vast majority are using the Native Development Kit (NDK): today to build efficient and portable code is crucial for most mobile developers. Rust is rapidly becoming a point of reference for all those who want to build portable code that is safe and with high performance needs.

This tutorial introduces Android developers to use Rust within Android application using:
- Android SDK+NDK
- Rust command `cargo apk` provided by [android-rs-glue], to compile and package the Rust code into an Android apk
- Rust crate `android_glue`, also provided by [android-rs-glue], to bind Rust code to the Android environment.

The result of this tutorial will be a full screen application.


## Non-goals

What's out of scope for this book:

- Teaching Rust.
- Teaching Android.
- Interaction between Rust code and Android managed code (eg. written in Java or Kotlin).
 This feature in Android is achieved through the JNI (Java Native Interface), and it is covered in more detail in this [rust-ios-android tutorial] by kennytm.

[rust-ios-android tutorial]: https://github.com/kennytm/rust-ios-android

## Thanks to
Meetup Roma-Roma for revision and the great support.

Codemotion for the opportunity to talk about this project to a wonderful audience!

## References
[android-rs-glue]: https://github.com/tomaka/android-rs-glue
[Taking Rust everywhere with rustup]:https://blog.rust-lang.org/2016/05/13/rustup.html#example-running-rust-on-android
[Announcing cargo-apk]: https://users.rust-lang.org/t/announcing-cargo-apk/5501
