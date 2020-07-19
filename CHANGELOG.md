# Change log

## 0.6.3+9

* Android: Add checks for hardware and enrollment
* Refactor fingerprint to more generic biometric

## 0.6.3+8

* Android: Add result listener to registrar in constructor

## 0.6.3+7

* Android: Add `getActivity()` method to avoid null error

## 0.6.3+6

* Android: Use binding to fetch current activity

## 0.6.3+5

* Android: Use application context when creating intent

## 0.6.3+4

* Cancel authentication even when biometric prompt not used

## 0.6.3+3

* Handles authentication for API 23 and up
* Returns unsupported status if device is using API 22 or below

## 0.6.3+2

* Bug fix: set Android variable authInProgress to false when authentication cancelled

## 0.6.3+1

* Handle `.isDeviceSupported()` on ios (always true)

## 0.6.3

* Add method `.isDeviceSupported()` to determine if device is supported.
  * Supports Android 9.0 or higher
  * Supports below Android 9.0 only if fingerprint reader hardware available

## 0.6.2+4

* Fix issues in older versions of android
* Return not supported error for Android 8 or older that do not have biometric hardware

## 0.6.2+3

* Failover to device credentials only if biometrics are not available
  * This is a work around for <https://issuetracker.google.com/issues/142740104>

## 0.6.2+2

* Update auth string to be more generic

## 0.6.2+1

* Fix bug with package name

## 0.6.2

* Add `authenticate` method that uses biometric authentication, but allows users to also use device authentication - pin, pattern, passcode.

## From [local_auth](https://github.com/flutter/plugins/tree/master/packages/package_info)

## 0.6.1+2

* Support v2 embedding.

## 0.6.1+1

* Remove the deprecated `author:` field from pubspec.yaml
* Migrate the plugin to the pubspec platforms manifest.
* Require Flutter SDK 1.10.0 or greater.

## 0.6.1

* Added ability to stop authentication (For Android).

## 0.6.0+3

* Remove AndroidX warnings.

## 0.6.0+2

* Update and migrate iOS example project.
* Define clang module for iOS.

## 0.6.0+1

* Update the `intl` constraint to ">=0.15.1 <0.17.0" (0.16.0 isn't really a breaking change).

## 0.6.0

* Define a new parameter for signaling that the transaction is sensitive.
* Up the biometric version to beta01.
* Handle no device credential error.

## 0.5.3

* Add face id detection as well by not relying on FingerprintCompat.

## 0.5.2+4

* Update README to fix syntax error.

## 0.5.2+3

* Update documentation to clarify the need for FragmentActivity.

## 0.5.2+2

* Add missing template type parameter to `invokeMethod` calls.
* Bump minimum Flutter version to 1.5.0.
* Replace invokeMethod with invokeMapMethod wherever necessary.

## 0.5.2+1
* Use post instead of postDelayed to show the dialog onResume.

## 0.5.2
* Executor thread needs to be UI thread.

## 0.5.1
* Fix crash on Android versions earlier than 28.
* [`authenticateWithBiometrics`](https://pub.dev/documentation/local_auth/latest/local_auth/LocalAuthentication/authenticateWithBiometrics.html) will not return result unless Biometric Dialog is closed.
* Added two more error codes `LockedOut` and `PermanentlyLockedOut`.

## 0.5.0
 * **Breaking change**. Update the Android API to use androidx Biometric package. This gives
   the prompt the updated Material look. However, it also requires the activity to be a
   FragmentActivity. Users can switch to FlutterFragmentActivity in their main app to migrate.

## 0.4.0+1

* Log a more detailed warning at build time about the previous AndroidX
  migration.

## 0.4.0

* **Breaking change**. Migrate from the deprecated original Android Support
  Library to AndroidX. This shouldn't result in any functional changes, but it
  requires any Android apps using this plugin to [also
  migrate](https://developer.android.com/jetpack/androidx/migrate) if they're
  using the original support library.

## 0.3.1
* Fix crash on Android versions earlier than 24.

## 0.3.0

* **Breaking change**. Add canCheckBiometrics and getAvailableBiometrics which leads to a new API.

## 0.2.1

* Updated Gradle tooling to match Android Studio 3.1.2.

## 0.2.0

* **Breaking change**. Set SDK constraints to match the Flutter beta release.

## 0.1.2

* Fixed Dart 2 type error.

## 0.1.1

* Simplified and upgraded Android project template to Android SDK 27.
* Updated package description.

## 0.1.0

* **Breaking change**. Upgraded to Gradle 4.1 and Android Studio Gradle plugin
  3.0.1. Older Flutter projects need to upgrade their Gradle setup as well in
  order to use this version of the plugin. Instructions can be found
  [here](https://github.com/flutter/flutter/wiki/Updating-Flutter-projects-to-Gradle-4.1-and-Android-Studio-Gradle-plugin-3.0.1).

## 0.0.3

* Add FLT prefix to iOS types

## 0.0.2+1

* Update messaging to support Face ID.

## 0.0.2

* Support stickyAuth mode.

## 0.0.1

* Initial release of local authentication plugin.
