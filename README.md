# React Native [Web] + Monorepo

## 100% code sharing between Web, iOS and Android

This is the source code from [this tutorial](https://dev.to/brunolemos/tutorial-100-code-sharing-between-ios-android--web-using-react-native-web-andmonorepo-4pej).

![article-cover](https://user-images.githubusercontent.com/619186/64933790-1fc27680-d81d-11e9-8077-64a1066b7c17.png)

### How to run

_Requirements: [React Native](https://facebook.github.io/react-native/docs/getting-started.html#native) (last tested on react-native@0.61)_

- `$ git clone git@github.com:brunolemos/react-native-web-monorepo.git`
- `$ cd react-native-web-monorepo`
- `$ yarn`
- `$ cd packages/mobile/ios`
- `$ pod install`
- `$ cd -`
- `$ yarn workspace web start`
- `$ yarn workspace mobile start`
- Run the project
  - [iOS] Via Xcode
    - `yarn xcode` (open the project on Xcode)
    - Press the Run button
  - [Android] Via Android Studio
    - `yarn studio` (open the project on Android Studio)
    - Press the Run button
  - Via CLI
    - _You may need to launch your device emulator before the next command_
    - `$ yarn android` or `$ yarn ios`

### Tips

- To install new dependencies, use the command `$yarn workspace components add xxx` from the root directory. To run a script from a package, run `$yarn workspace web start`, for example; To run a script from all packages, run `$yarn workspaces run scriptname`;

- If React Native starts getting installed inside packages/mobile/node_modules, this is wrong. You need to make sure all your dependencies have the exact same version between the monorepo packages. For example, change your "react" dependency inside the mobile and web's package.json to the exact same version (e.g. 16.8.4).
  This will make react-native get installed in the root node_modules again and also prevent multiple instances of react being installed in the same project, which would cause all kinds of bugs.

## Who is using this on production

Check out [DevHub](https://github.com/devhubapp/devhub).
The main difference is that it supports Desktop (Electron) in addition to Web, iOS and Android.

![DevHub Desktop](https://user-images.githubusercontent.com/619186/63945240-59d40000-ca49-11e9-98c1-353225f8dcf6.jpg)

![DevHub Menubar](https://github.com/devhubapp/devhub/raw/master/landing/static/screenshots/devhub-desktop-menubar-banner.jpg)

<p align="center">
  <img alt="DevHub Mobile - Notifications" height="620" src="https://github.com/devhubapp/devhub/raw/master/landing/static/screenshots/iphone-notifications-dark.jpg" />
  <img alt="DevHub Mobile - Notification Filters" height="620" src="https://github.com/devhubapp/devhub/raw/master/landing/static/screenshots/iphone-notifications-filters-dark.jpg" />
  <img alt="DevHub Mobile - Events" height="620" src="https://github.com/devhubapp/devhub/raw/master/landing/static/screenshots/iphone-events-dark.jpg" />
</p>

<br/>
