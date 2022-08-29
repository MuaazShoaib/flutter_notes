# 06 - MiCard - How to Build Beautiful UIs with Flutter Widgets

## 001 MiCard - A Single Screen Personal Business Card App


```
// main.dart

// 001 MiCard - A Single Screen Personal Business Card App

// Clone Mi Card Project

// git clone https://github.com/londonappbrewery/mi_card_flutter.git

import 'package:flutter/material.dart';

void main() {
  runApp(
    MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.teal,
        body: Container(),
      ),
    ),
  );
}

```

## 002 Hot Reload and Hot Restart - Flutter Power Tools

```
// main.dart

// 002 Hot Reload and Hot Restart - Flutter Power Tools

import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

// Hot Reload & Hot Restart works in StatelessWidget or StatefulWidget

// shortcut to create StatelessWidget is 'stless'

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        // backgroundColor: Colors.teal,
        // backgroundColor: Colors.red,
        // backgroundColor: Colors.blue,
        backgroundColor: Colors.white,
        body: Container(),
      ),
    );
  }
}
```
## 003 How to Use Container Widgets
```
// main.dart

// 003 How to Use Container Widgets

import 'package:flutter/cupertino.dart';
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.teal,
        body: SafeArea(
          child: Container(
            height: 100.0,
            width: 100.0,
            // margin: EdgeInsets.all(20.0),
            // margin: EdgeInsets.symmetric(vertical: 50.0, horizontal: 10.0),
            // margin: EdgeInsets.fromLTRB(10.0, 20.0, 30.0, 40.0),
            margin: EdgeInsets.only(left: 30.0),
            // margin: is used for parent i.e Container
            // padding: is used for child i.e Text
            padding: EdgeInsets.all(20.0),
            color: Colors.white,
            child: Text('Hello'),
          ),
        ),
      ),
    );
  }
}
```

## 004 How to use Column & Row Widgets for Layout

```
// main.dart

// 004 How to use Column & Row Widgets for Layout

import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.teal,
        body: SafeArea(
          // child: Column(
          //   // mainAxisSize: MainAxisSize.min,
          //   // verticalDirection: VerticalDirection.up,
          //   // verticalDirection: VerticalDirection.down,
          //   // mainAxisAlignment: MainAxisAlignment.start,
          //   // mainAxisAlignment: MainAxisAlignment.end,
          //   // mainAxisAlignment: MainAxisAlignment.center,
          //   // mainAxisAlignment: MainAxisAlignment.spaceEvenly,
          //   // mainAxisAlignment: MainAxisAlignment.spaceBetween,
          //   // crossAxisAlignment: CrossAxisAlignment.start,
          //   // crossAxisAlignment: CrossAxisAlignment.end,
          //   crossAxisAlignment: CrossAxisAlignment.stretch,
          //   children: [
          //     Container(
          //       height: 100.0,
          //       // width: 100.0,
          //       // width: double.infinity,
          //       color: Colors.white,
          //       child: Text('Container 1'),
          //     ),
          //     SizedBox(
          //       height: 20.0,
          //     ),
          //     Container(
          //       height: 100.0,
          //       // width: 100.0,
          //       // width: 300.0,
          //       // width: double.infinity,
          //       color: Colors.blue,
          //       child: Text('Container 2'),
          //     ),
          //     Container(
          //       height: 100.0,
          //       // width: 100.0,
          //       // width: double.infinity,
          //       color: Colors.red,
          //       child: Text('Container 3'),
          //     ),
          //     // Container(
          //     //   width: double.infinity,
          //     //   height: 10.0,
          //     // ),
          //   ],
          // ),

          child: Row(
            // mainAxisSize: MainAxisSize.min,
            // verticalDirection: VerticalDirection.up,
            // verticalDirection: VerticalDirection.down,
            // mainAxisAlignment: MainAxisAlignment.start,
            // mainAxisAlignment: MainAxisAlignment.end,
            // mainAxisAlignment: MainAxisAlignment.center,
            // mainAxisAlignment: MainAxisAlignment.spaceEvenly,
            // mainAxisAlignment: MainAxisAlignment.spaceBetween,
            // crossAxisAlignment: CrossAxisAlignment.start,
            // crossAxisAlignment: CrossAxisAlignment.end,
            crossAxisAlignment: CrossAxisAlignment.stretch,
            children: [
              Container(
                // height: 100.0,
                // width: 100.0,
                // width: double.infinity,
                width: 30.0,
                color: Colors.white,
                child: Text('Container 1'),
              ),
              SizedBox(
                width: 20.0,
              ),
              Container(
                // height: 100.0,
                // width: 100.0,
                // width: 300.0,
                // width: double.infinity,
                color: Colors.blue,
                child: Text('Container 2'),
              ),
              Container(
                // height: 100.0,
                // width: 100.0,
                // width: double.infinity,
                color: Colors.red,
                child: Text('Container 3'),
              ),
              // Container(
              //   width: double.infinity,
              //   height: 10.0,
              // ),
            ],
          ),
        ),
      ),
    );
  }
}
```

## 005 Flutter Layouts Challenge
Flutter Layout Challenge: https://github.com/MuaazShoaib/flutter_layout_challenge	

## 006 Tapping into Widget Properties

```
// main.dart

// 006 Tapping into Widget Properties

import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.teal,
        body: SafeArea(
          child: Column(
            children: [
              // For Quick Documentation: Ctrl + Q

              CircleAvatar(
                radius: 50.0,
                // backgroundColor: Colors.red,
                backgroundImage: AssetImage('images/muaaz.jpg'),
              ),
              Text(
                'Muaaz Shoaib',
                style: TextStyle(
                  fontSize: 40.0,
                  color: Colors.white,
                  fontWeight: FontWeight.bold,
                ),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
```

```
# pubspec.yaml

# 006 Tapping into Widget Properties

name: mi_card
description: A new Flutter project.

# The following line prevents the package from being accidentally published to
# pub.dev using `flutter pub publish`. This is preferred for private packages.
publish_to: 'none' # Remove this line if you wish to publish to pub.dev

# The following defines the version and build number for your application.
# A version number is three numbers separated by dots, like 1.2.43
# followed by an optional build number separated by a +.
# Both the version and the builder number may be overridden in flutter
# build by specifying --build-name and --build-number, respectively.
# In Android, build-name is used as versionName while build-number used as versionCode.
# Read more about Android versioning at https://developer.android.com/studio/publish/versioning
# In iOS, build-name is used as CFBundleShortVersionString while build-number used as CFBundleVersion.
# Read more about iOS versioning at
# https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/CoreFoundationKeys.html
version: 1.0.0+1

environment:
  sdk: ">=2.16.1 <3.0.0"

# Dependencies specify other packages that your package needs in order to work.
# To automatically upgrade your package dependencies to the latest versions
# consider running `flutter pub upgrade --major-versions`. Alternatively,
# dependencies can be manually updated by changing the version numbers below to
# the latest version available on pub.dev. To see which dependencies have newer
# versions available, run `flutter pub outdated`.
dependencies:
  flutter:
    sdk: flutter


  # The following adds the Cupertino Icons font to your application.
  # Use with the CupertinoIcons class for iOS style icons.
  cupertino_icons: ^1.0.2

dev_dependencies:
  flutter_test:
    sdk: flutter

  # The "flutter_lints" package below contains a set of recommended lints to
  # encourage good coding practices. The lint set provided by the package is
  # activated in the `analysis_options.yaml` file located at the root of your
  # package. See that file for information about deactivating specific lint
  # rules and activating additional ones.
  flutter_lints: ^1.0.0

# For information on the generic Dart part of this file, see the
# following page: https://dart.dev/tools/pub/pubspec

# The following section is specific to Flutter.
flutter:

  # The following line ensures that the Material Icons font is
  # included with your application, so that you can use the icons in
  # the material Icons class.
  uses-material-design: true

  # Create a new directory 'images'
  # Put images in the images directory
  # To add assets to your application, add an assets section, like this:
  assets:
#    - images/
    - images/muaaz.jpg

  # An image asset can refer to one or more resolution-specific "variants", see
  # https://flutter.dev/assets-and-images/#resolution-aware.

  # For details regarding adding assets from package dependencies, see
  # https://flutter.dev/assets-and-images/#from-packages

  # To add custom fonts to your application, add a fonts section here,
  # in this "flutter" section. Each entry in this list should have a
  # "family" key with the font family name, and a "fonts" key with a
  # list giving the asset and other descriptors for the font. For
  # example:
  # fonts:
  #   - family: Schyler
  #     fonts:
  #       - asset: fonts/Schyler-Regular.ttf
  #       - asset: fonts/Schyler-Italic.ttf
  #         style: italic
  #   - family: Trajan Pro
  #     fonts:
  #       - asset: fonts/TrajanPro.ttf
  #       - asset: fonts/TrajanPro_Bold.ttf
  #         weight: 700
  #
  # For details regarding fonts from package dependencies,
  # see https://flutter.dev/custom-fonts/#from-packages
```

## 007 Incorporating Custom Fonts in Your Flutter App
```
// main.dart

// 007 Incorporating Custom Fonts in Your Flutter App

import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.teal,
        body: SafeArea(
          child: Column(
            children: [
              // For Quick Documentation: Ctrl + Q

              CircleAvatar(
                radius: 50.0,
                // backgroundColor: Colors.red,
                backgroundImage: AssetImage('images/muaaz.jpg'),
              ),
              Text(
                'Muaaz Shoaib',
                style: TextStyle(
                  fontFamily: 'Pacifico',
                  fontSize: 40.0,
                  color: Colors.white,
                  fontWeight: FontWeight.bold,
                ),
              ),
              Text(
                'FLUTTER DEVELOPER',
                style: TextStyle(
                  fontFamily: 'Source Sans Pro',
                  // color: Colors.teal[100],
                  color: Colors.teal.shade100,
                  fontSize: 20.0,
                  letterSpacing: 2.5,
                  fontWeight: FontWeight.bold,
                ),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
```

```
# pubspec.yaml

# 007 Incorporating Custom Fonts in Your Flutter App

name: mi_card
description: A new Flutter project.

# The following line prevents the package from being accidentally published to
# pub.dev using `flutter pub publish`. This is preferred for private packages.
publish_to: 'none' # Remove this line if you wish to publish to pub.dev

# The following defines the version and build number for your application.
# A version number is three numbers separated by dots, like 1.2.43
# followed by an optional build number separated by a +.
# Both the version and the builder number may be overridden in flutter
# build by specifying --build-name and --build-number, respectively.
# In Android, build-name is used as versionName while build-number used as versionCode.
# Read more about Android versioning at https://developer.android.com/studio/publish/versioning
# In iOS, build-name is used as CFBundleShortVersionString while build-number used as CFBundleVersion.
# Read more about iOS versioning at
# https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/CoreFoundationKeys.html
version: 1.0.0+1

environment:
  sdk: ">=2.16.1 <3.0.0"

# Dependencies specify other packages that your package needs in order to work.
# To automatically upgrade your package dependencies to the latest versions
# consider running `flutter pub upgrade --major-versions`. Alternatively,
# dependencies can be manually updated by changing the version numbers below to
# the latest version available on pub.dev. To see which dependencies have newer
# versions available, run `flutter pub outdated`.
dependencies:
  flutter:
    sdk: flutter


  # The following adds the Cupertino Icons font to your application.
  # Use with the CupertinoIcons class for iOS style icons.
  cupertino_icons: ^1.0.2

dev_dependencies:
  flutter_test:
    sdk: flutter

  # The "flutter_lints" package below contains a set of recommended lints to
  # encourage good coding practices. The lint set provided by the package is
  # activated in the `analysis_options.yaml` file located at the root of your
  # package. See that file for information about deactivating specific lint
  # rules and activating additional ones.
  flutter_lints: ^1.0.0

# For information on the generic Dart part of this file, see the
# following page: https://dart.dev/tools/pub/pubspec

# The following section is specific to Flutter.
flutter:

  # The following line ensures that the Material Icons font is
  # included with your application, so that you can use the icons in
  # the material Icons class.
  uses-material-design: true

  # Create a new directory 'images'
  # Put images in the images directory
  # To add assets to your application, add an assets section, like this:
  assets:
#    - images/
    - images/muaaz.jpg

  # An image asset can refer to one or more resolution-specific "variants", see
  # https://flutter.dev/assets-and-images/#resolution-aware.

  # For details regarding adding assets from package dependencies, see
  # https://flutter.dev/assets-and-images/#from-packages

  # Download fonts from https://fonts.google.com/
  # Search Pacifico https://fonts.google.com/specimen/Pacifico
  # Search Source Sans Pro https://fonts.google.com/specimen/Source+Sans+Pro
  # Create a new directory 'fonts'
  # Put fonts in the fonts directory

  # To add custom fonts to your application, add a fonts section here,
  # in this "flutter" section. Each entry in this list should have a
  # "family" key with the font family name, and a "fonts" key with a
  # list giving the asset and other descriptors for the font. For
  # example:
  fonts:
    - family: Pacifico
      fonts:
        - asset: fonts/Pacifico-Regular.ttf

    - family: Source Sans Pro
      fonts:
        - asset: fonts/SourceSansPro-Regular.ttf

  #   - family: Trajan Pro
  #     fonts:
  #       - asset: fonts/TrajanPro.ttf
  #       - asset: fonts/TrajanPro_Bold.ttf
  #         weight: 700
  #
  # For details regarding fonts from package dependencies,
  # see https://flutter.dev/custom-fonts/#from-packages
```

## 008 Adding Material Icons with the Icon Widget
```
// main.dart

// 008 Adding Material Icons with the Icon Widget

import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.teal,
        body: SafeArea(
          child: Column(
            children: [
              // For Quick Documentation: Ctrl + Q

              CircleAvatar(
                radius: 50.0,
                // radius: 1000.0,
                // radius: 10000.0,
                // backgroundColor: Colors.red,
                backgroundImage: AssetImage('images/muaaz.jpg'),
              ),
              Text(
                'Muaaz Shoaib',
                style: TextStyle(
                  fontFamily: 'Pacifico',
                  fontSize: 40.0,
                  color: Colors.white,
                  fontWeight: FontWeight.bold,
                ),
              ),
              Text(
                'FLUTTER DEVELOPER',
                style: TextStyle(
                  fontFamily: 'Source Sans Pro',
                  // color: Colors.teal[100],
                  color: Colors.teal.shade100,
                  fontSize: 20.0,
                  letterSpacing: 2.5,
                  fontWeight: FontWeight.bold,
                ),
              ),
              Container(
                color: Colors.white,
                margin: EdgeInsets.symmetric(vertical: 10.0, horizontal: 25.0),
                padding: EdgeInsets.all(10.0),
                child: Row(
                  children: [
                    Icon(
                      // Icons.add_shopping_cart,
                      Icons.phone,
                      color: Colors.teal,
                      // size: 100.0,
                      // size: 1000.0,
                    ),
                    SizedBox(
                      width: 10.0,
                    ),
                    Text(
                      '+92 123 456 789',
                      style: TextStyle(
                        color: Colors.teal.shade900,
                        fontFamily: 'Source Sans Pro',
                        fontSize: 20.0,
                      ),
                    ),
                  ],
                ),
              ),
              Container(
                padding: EdgeInsets.all(10.0),
                margin: EdgeInsets.symmetric(vertical: 10.0, horizontal: 25.0),
                color: Colors.white,
                child: Row(
                  children: [
                    Icon(
                      Icons.email,
                      color: Colors.teal,
                    ),
                    SizedBox(
                      width: 10.0,
                    ),
                    Text(
                      'example@email.com',
                      style: TextStyle(
                        fontFamily: 'Source Sans Pro',
                        color: Colors.teal.shade900,
                        fontSize: 20.0,
                      ),
                    ),
                  ],
                ),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
```

## 009 Flutter Card & ListTile Widgets
```
// main.dart

// 009 Flutter Card & ListTile Widgets

import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.teal,
        body: SafeArea(
          child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              // For Quick Documentation: Ctrl + Q

              CircleAvatar(
                radius: 50.0,
                // radius: 1000.0,
                // radius: 10000.0,
                // backgroundColor: Colors.red,
                backgroundImage: AssetImage('images/muaaz.jpg'),
              ),
              Text(
                'Muaaz Shoaib',
                style: TextStyle(
                  fontFamily: 'Pacifico',
                  fontSize: 40.0,
                  color: Colors.white,
                  fontWeight: FontWeight.bold,
                ),
              ),
              Text(
                'FLUTTER DEVELOPER',
                style: TextStyle(
                  fontFamily: 'Source Sans Pro',
                  // color: Colors.teal[100],
                  color: Colors.teal.shade100,
                  fontSize: 20.0,
                  letterSpacing: 2.5,
                  fontWeight: FontWeight.bold,
                ),
              ),
              SizedBox(
                height: 20.0,
                width: 150.0,
                child: Divider(
                  color: Colors.teal.shade100,
                ),
              ),

              Card(
                // color: Colors.white,
                margin: EdgeInsets.symmetric(vertical: 10.0, horizontal: 25.0),

                // You can add padding to Card by wrapping it with Padding: Alt + Enter

                // child: Padding(
                //   padding: const EdgeInsets.all(8.0),
                //   child: Row(
                //     children: [
                //       Icon(
                //         // Icons.add_shopping_cart,
                //         Icons.phone,
                //         color: Colors.teal,
                //         // size: 100.0,
                //         // size: 1000.0,
                //       ),
                //       SizedBox(
                //         width: 10.0,
                //       ),
                //       Text(
                //         '+92 123 456 789',
                //         style: TextStyle(
                //           color: Colors.teal.shade900,
                //           fontFamily: 'Source Sans Pro',
                //           fontSize: 20.0,
                //         ),
                //       ),
                //     ],
                //   ),
                // ),

                child: ListTile(
                  leading: Icon(
                    // Icons.add_shopping_cart,
                    Icons.phone,
                    color: Colors.teal,
                    // size: 100.0,
                    // size: 1000.0,
                  ),
                  title: Text(
                    '+92 123 456 789',
                    style: TextStyle(
                      color: Colors.teal.shade900,
                      fontFamily: 'Source Sans Pro',
                      fontSize: 20.0,
                    ),
                  ),
                ),
              ),

              Card(
                margin: EdgeInsets.symmetric(vertical: 10.0, horizontal: 25.0),
                // color: Colors.white,
                // child: Row(
                //   children: [
                //     Icon(
                //       Icons.email,
                //       color: Colors.teal,
                //     ),
                //     SizedBox(
                //       width: 10.0,
                //     ),
                //     Text(
                //       'example@email.com',
                //       style: TextStyle(
                //         fontFamily: 'Source Sans Pro',
                //         color: Colors.teal.shade900,
                //         fontSize: 20.0,
                //       ),
                //     ),
                //   ],
                // ),
                child: ListTile(
                  leading: Icon(
                    Icons.email,
                    color: Colors.teal,
                  ),
                  title: Text(
                    'example@email.com',
                    style: TextStyle(
                      fontFamily: 'Source Sans Pro',
                      color: Colors.teal.shade900,
                      fontSize: 20.0,
                    ),
                  ),
                ),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
```

# Your Project for this Section
