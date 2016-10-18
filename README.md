Android Upload Service
======================

[![](https://jitpack.io/v/NaikSoftware/android-upload-service.svg)](https://jitpack.io/#NaikSoftware/android-upload-service)

![Upload Notification](http://gotev.github.io/android-upload-service/upload.gif)

Easily upload files in the background with automatic Android Notification Center progress indication.

## Purpose
* have a tiny library (less than 60KB)
* upload files to a server with HTTP
* support upload through path from ContentProvider Uri (pass Uri.toString as parameter) or absolute file path
* be able to easily implement other upload protocols as plugins
* handle multiple concurrent uploads in the background, even if the device is idle
* automatically retry failed uploads, with a configurable exponential backoff
* possibility to automatically delete uploaded files when the upload is successful
* show status in the Android Notification Center (with support for [stacking notifications](http://developer.android.com/training/wearables/notifications/stacks.html)).
* be able to change the underlying HTTP stack. Currently `HttpURLConnection` (the default) and `OkHttp` are supported. You can also implement your own.
* be able to set library log level and to provide custom logger implementation

At the core of the library there is a `Service` which handles multiple concurrent upload tasks in the background. It publishes broadcast intents to notify status. This way the logic is completely decoupled from the UI. Read further to learn how you can use it in your App.

## Getting started <a name="setup"></a>
[Read this page](https://github.com/gotev/android-upload-service/wiki/Setup) for full setup instructions with Maven and Gradle.

[Check the wiki](https://github.com/gotev/android-upload-service/wiki) to discover how to get started.

[Check JavaDocs](http://gotev.github.io/android-upload-service/javadoc/) for a complete reference of the library's API

Do you need help? [Read this](https://github.com/gotev/android-upload-service/wiki/Asking%20for%20help)

## Apps powered by Android Upload Service <a name="powered"></a>
To be included in the following list, simply create an issue and provide the app name and a link.

- [VoiSmart IP Communicator](https://play.google.com/store/apps/details?id=com.voismart.softphone)
- [Motolife](https://play.google.com/store/apps/details?id=bg.motolife.app)
- [NativeScript Background HTTP](https://www.npmjs.com/package/nativescript-background-http)

## Contributing <a name="contribute"></a>
* Do you have a new feature in mind?
* Do you know how to improve existing docs or code?
* Have you found a bug?

Contributions are welcome and encouraged! Just fork the project and then send a pull request. Be ready to discuss your code and design decisions.

## License <a name="license"></a>

    Copyright (C) 2013-2016 Aleksandar Gotev, Nickolay Savchenko

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
