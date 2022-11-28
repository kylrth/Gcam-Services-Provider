# Gcam Services Provider

[![continuous](https://github.com/lukaspieper/Gcam-Services-Provider/workflows/continuous/badge.svg)](https://github.com/lukaspieper/Gcam-Services-Provider/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/lukaspieper/Gcam-Services-Provider/blob/master/LICENSE)

This app "simulates" the Google Play Services that the Google Camera app (Gcam) requires, allowing the camera app to be used on devices without Google Play Services.

### Comparison: [GrapheneOS' Sandboxed Play services](https://grapheneos.org/usage#sandboxed-play-services)

Back in July 2021, GrapheneOS implemented a compatibility layer to use the original Google Play services without advanced permissions. This offers another possibility to make Gcam work. For Gcam it is sufficient to install the Google Service Framework (GSF). Optionally revoke the Internet permission, it is not needed for Gcam. <ins>If you already use this feature, or you plan to use an app that requires Play services, you cannot use the Gcam Services Provider for technical reasons. This limitation applies beyond the boundaries of a user profile.</ins> Otherwise, you have a choice. There is no difference in terms of security, both apps run in the same sandbox environment. **However, this app allows you to use the button in Gcam that opens the last taken photo without having Google Photos installed.**

Read more about using Gcam with Sandboxed Play services on their [documentation](https://grapheneos.org/usage#google-camera).

### Comparison: [microG](https://github.com/microg)

microG is a open source re-implementation of the Google Play Services (client side). Among other things, [signature spoofing](https://github.com/microg/android_packages_apps_GmsCore/wiki/Signature-Spoofing) is used to achieve this goal. In comparison, this app only aims to get Gcam running without Play Services. Therefore this app does not need any security compromising hacks or permissions (no Internet access, no storage access and of course no root access).

## How to install this app?

> Using GrapheneOS? Make sure you read the comparison with GrapheneOS' Sandboxed Play services above!

Currently there are two versions of this app named "basic" and "photos". "Basic" includes everything you need to get Gcam running but the button showing the last taken photo in full size will not work. The "photos" version has all features from "basic" and adds support for this button but you cannot have the Google Photos app installed for technical reasons.

Note that this app comes without UI and therefore has no icon in the app drawer. But of course it is listed in the Android settings (e.g. for uninstallation).

|                | Incompatible apps                                           | Download           |
|----------------|-------------------------------------------------------------|--------------------|
| Basic version  | - Google Service Framework (GSF)<br/>- microg                     | [GitHub](https://github.com/lukaspieper/Gcam-Services-Provider/releases)<br/>[F-Droid](https://f-droid.org/de/packages/de.lukaspieper.gcam.services/) |
| Photos version | - Google Service Framework (GSF)<br/>- microg<br/>- Google Photos | [GitHub](https://github.com/lukaspieper/Gcam-Services-Provider/releases)             |

### Gcam Compatibility

|Google camera version|Requirements                        |Relevant issues                                                                              |
|---------------------|------------------------------------|---------------------------------------------------------------------------------------------|
|7.4 & 7.5            |                                    |                                                                                             |
|>=7.6                |Compatible Android OS or modded Gcam|[#22](https://github.com/lukaspieper/Gcam-Services-Provider/issues/22#issuecomment-814239882)|

## Known from/recommended by

- [XDA Developers](https://www.xda-developers.com/google-camera-port-hub/)
- [GCam Hub (celsoazevedo)](https://www.celsoazevedo.com/files/android/google-camera/troubleshooting/)
- [Kuketz-Blog (German IT security and privacy blog)](https://www.kuketz-blog.de/?s=gcam+services+provider)
