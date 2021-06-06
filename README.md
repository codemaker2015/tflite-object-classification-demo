# TensorFlow Lite Object Classification Demo

Porting of ["TensorFlow Lite Examples"](https://www.tensorflow.org/lite/examples) to Unity.

Tested on  

- Android / Windows  
- Unity 2019.4.17f1
- TensorFlow 2.4.0

Samples

- TensorFlow
  - SSD Object Detection

Included prebuilt libraries

| | iOS | Android | macOS | Ubuntu | Windows |
|---|:---:|:---:|:---:|:---:|:---:|
| Core CPU |✅|✅|✅|✅|✅|
| Metal Delegate |✅| - |✅| - | - |
| OpenGL Delegate | - |✅| - | - | - |
| NNAPI Delegate | - |✅| - | - | - |

- All libraries except iOS are targeted 64bit platform: arm64 or x86_64.

## Install TensorFlow Lite for Unity

- Clone this repository with examples
  - Requires installing [Git-LFS](https://git-lfs.github.com/)
- The TFLite core library is available on:
  - [OpenUPM](https://openupm.com/packages/com.github.asus4.tflite/)  
  Run `openupm add com.github.asus4.tflite` from the command line.
  - Or add git URL from the Package Maneger UI: `https://github.com/asus4/tf-lite-unity-sample.git?path=/Packages/com.github.asus4.tflite`

## Build TensorFlow Lite libraries

Pre-built libraries are included. If you want to build the latest TFLite,

1. Clone [TensorFlow library](https://github.com/tensorflow/tensorflow/)
2. Run `./configure` in the TensorFlow library
3. Run `./build_tflite.py` (Python3) to build for each platform

  ```sh
  # Update iOS, Andoid and macOS
  ./build_tflte.py --tfpath ../tensorflow -ios -android -macos

  # Build with XNNPACK
  ./build_tflte.py --tfpath ../tensorflow -macos -xnnpack
  ```

## TIPS

\[Android\] You can see logs from tflite by filtering with "tflite"  

```bash
# Filtering logcat only Unity and tflite
adb logcat Unity:V tflite:V "*:S"
```

## Demo

| Screenshot | Demo video |
|:---:|:---:|
| ![screenshtot](https://github.com/codemaker2015/tflite-object-classification-demo/blob/master/Demo/demo2.gif) | ![screenshtot](https://github.com/codemaker2015/tflite-object-classification-demo/blob/master/Demo/demo.gif) |

