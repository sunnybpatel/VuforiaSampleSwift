# VuforiaSampleSwift

Vuforia sample code with SceneKit using Swift.

## Requirement

* Xcode 7.3.1
* iOS 9.3.2
* Vuforia SDK for iOS v5.5.9

## Usage

See ViewController.swift.

``` swift

vuforiaManager = VuforiaManager(licenseKey: "your license key", dataSetFile: "your target xml file")
if let manager = vuforiaManager {
    manager.delegate = self
    manager.eaglView.sceneSource = self
    manager.eaglView.delegate = self
    manager.eaglView.setupRenderer()
    self.view = manager.eaglView
}

vuforiaManager?.prepareWithOrientation(.Portrait)

...

do {
    try vuforiaManager?.start()
}catch let error {
    print("\(error)")
}

```

## ScreenShot

![screenshot](https://github.com/yshrkt/VuforiaSampleSwift/blob/master/screenshot.jpg)

## Thanks

I am referring to the following page.

* [Making Augmented Reality app easily with Scenekit + Vuforia (in English)](http://qiita.com/akira108/items/a743138fca532ee193fe)