
Cordova Print Plugin - Example
==============================

[Cordova][cordova] plugin to print HTML documents using [__AirPrint__][AirPrint]  and [__Google Cloud Print__][GCP].

## Instructions
[Download][zip] the _example-google-cloud-print_ branch and run the following command:

```bash
cordova emulate [ios|android]
```

These will lunch the simulator or any plugged in device and start the example application as seen below in the screenshots. Its also possible to open the project with [Android Studio][studio] or [Eclipse][eclipse].

A click on the _PRINT SOME STUFF_ link opens the native print dialog to print out an HTML snippet.

```javascript
page = '';

page += '<h1>This is a main header<h1>';
page += '<h2>Thats a sub category</h2>';

cordova.plugins.printer.print(page, { landscape:false }, function () {
    alert('done');
});
```

Please read the plugin's [README][readme] for further requirements and informations.


### Testing in the iOS Simulator
There's no need to waste lots of paper when testing - if you're using the iOS simulator, select _File -> Open Printer Simulator_ to open some dummy printers (print outs will appear as PDF files).


### Testing in the Android Simulator
There's no need to waste lots of paper when testing - if you're using the Android simulator, select _Save to PDF_.

Dont forget to install a PDF viewer like [MuPDF][mupdf], otherwise Android will not open the file. Note that you need to install the app for the right hardware architecture!


## Screenshots iOS
![ios][ios_screens]


## Screenshots Android
![android][android_screens]


## License

This software is released under the [Apache 2.0 License][apache2_license].

© 2013-2014 appPlant UG, Inc. All rights reserved


[cordova]: https://cordova.apache.org
[GCP]: http://www.google.com/cloudprint/learn/index.html
[AirPrint]: http://support.apple.com/kb/ht4356
[android_screens]: images/android.tiff
[ios_screens]: images/ios.tiff
[readme]: https://github.com/katzer/cordova-plugin-printer/blob/google-cloud-print/README.md
[zip]: https://github.com/katzer/cordova-plugin-printer/archive/google-cloud-print.zip
[studio]: https://developer.android.com/sdk/installing/studio.html
[eclipse]: https://developer.android.com/sdk/index.html
[mupdf]: http://www.mupdf.com
[apache2_license]: http://opensource.org/licenses/Apache-2.0
