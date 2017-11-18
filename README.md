# TensorFlow (1.4.0) Image Classifier Gradle Standalone Port

- Clone the project, and checkout the tag `1.4.0`
- Import it on Android Studio
- Run it
- That's all.

This project is a way to get started with TensorFlow Image Classifier quickly.

I am not planning to maintain it. If you need an updated version, build it yourself using hints from this [blog post][blog-post].


## Native libraries

Native compiled libraries are embedded in the `1.4.0` tag, so you won't need to install the NDK.  
However, this means that you cannot change the `org.tensorflow.demo.env.ImageUtils` class.  
Here's what you need to do if you want, for example, to use a different package name:

* Install the [NDK and build tools][ndk]
* Checkout the `1.4.0-cmake` tag
* Modify line 7 of the `app/src/main/cpp/imageutils_jni.cpp` file to specify your new package name

[blog-post]: http://nilhcem.com/android/custom-tensorflow-classifier
[ndk]: https://developer.android.com/studio/projects/add-native-code.html
