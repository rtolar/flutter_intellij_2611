# flutter_intellij_2611

Code to reproduce bug report:
https://github.com/flutter/flutter-intellij/issues/2611

Title: "No exception information for analysis server errors."

Steps to reproduce this code:
1) Create new skeleton Flutter app using Android Studio
2) Update pubspec.yaml to add dep to http package
http: ^0.11.3+17
3) Update packages (e.g. 'pub upgrade' or click the 'update dependencies' message after modifying pubspec.yaml
4) Type ` var client = http.C` in main.dart

Android Studio reports a Dart Analyzer error.
It only does this the first time you type this code after starting Android Studio.
Restart Android Studio to get it to happen again.