# flutter_full_pdf_viewer_null_safe

PDF viewer for flutter , this repo is for of [flutter_full_pdf_viewer](https://pub.dev/packages/flutter_full_pdf_viewer)

Android and iOS working pdf viewer!

# Use this package as a library

## 1. Depend on it

Add this to your package's pubspec.yaml file:

```
dependencies:
  flutter_full_pdf_viewer_null_safe: ^1.0.0
```

### 2. Install it

You can install packages from the command line:

with Flutter:

```
$ flutter packages get
```

Alternatively, your editor might support pub get or `flutter packages get`. Check the docs for your editor to learn more.

### 3. Import it

Now in your Dart code, you can use:

```
import 'package:flutter_full_pdf_viewer_null_safe/full_pdf_viewer_scaffold.dart';
```

### 4. Informations for Release on Android

You have to follow first these steps: https://flutter.io/docs/deployment/android
After that you have to add ndk filters to your release config:

```
    buildTypes {

        release {
            signingConfig signingConfigs.release
            minifyEnabled true
            useProguard true
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'

            ndk {
                abiFilters 'armeabi-v7a'
            }
        }

        debug {
            minifyEnabled false
            useProguard false
        }
    }

```

Now your release app should work.
