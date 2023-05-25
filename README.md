# Flutter Keyboard Dismisser

A simple Flutter package to hide the keyboard when performing a gesture outside of it.

## Features

1. By default, dismisses the keyboard when tapping outside of it on an inactive widget.

2. Supports several gestures at the same time.

3. Supports all the gestures available in Flutter's GestureDetector.

4. Supports directional swipes to dismiss the keyboard.

5. Can be applied to a whole page by wrapping its Scaffold.

6. Can be applied to a whole app, by wrapping its MaterialApp, WidgetsApp, or CupertinoApp.

7. Customizable drag start behavior and gesture hit testing behavior.

8. Can be excluded from the semantics tree.

## Usage

This package exposes a KeyboardDismisser stateless widget. You can wrap your widget with it, and your widget will be able to dismiss the keyboard when performing a gesture.

   ```
   Widget build(BuildContext context) => KeyboardDismisser(
        child: Scaffold(
            body: ...,
        ),
      );
   ```

KeyboardDismisser takes a gestures parameter, which is a list of GestureType enum cases. This way, you can pass any gesture you like for the keyboard dismissal. By default, KeyboardDismisser will dismiss the keyboard when tapping outside of it, but it handles several gestures at the same time.

   ```
   Widget build(BuildContext context) => KeyboardDismisser(
        gestures: [GestureType.onTap, GestureType.onPanUpdateDownDirection],
        child: Scaffold(
            body: ...,
        ),
      );
   ```

## Getting started

In the pubspec.yaml of your flutter project, add the following dependency:

   ```
   dependencies:
  keyboard_dismisser: "^[LATEST_VERSION]"
   ```

Then run $ flutter pub get. In your library, add the following import:

   ```
   import 'package:keyboard_dismisser/keyboard_dismisser.dart';
   ```
