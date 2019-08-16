<p align="center" >
<h3 align="center">
  💬 UY Chat
</h3>
<p align="center">
  The most complete chat UI for React Native
</p>


## Sponsor

<p align="center">
  <br/>
  <p align="center">
    Coding Bootcamp in Paris co-founded by Farid Safi
  </p>
  <a href="https://www.lereacteur.io" target="_blank">
    <p align="center">
      Click to learn more
    </p>
  </a>
</p>

## Features

- Write with **TypeScript** (since 0.8.0)
- Fully customizable components
- Composer actions (to attach photos, etc.)
- Load earlier messages
- Copy messages to clipboard
- Touchable links using [react-native-parsed-text](https://github.com/taskrabbit/react-native-parsed-text)
- Avatar as user's initials
- Localized dates
- Multi-line TextInput
- InputToolbar avoiding keyboard
- Redux support
- System message
- Quick Reply messages (bot)

## Dependency

- Use version `0.2.x` for RN `>= 0.44.0`
- Use version `0.1.x` for RN `>= 0.40.0`
- Use version `0.0.10` for RN `< 0.40.0`


## Notes for Android

If you are using Create React Native App / Expo, no Android specific installation steps are required -- you can skip this section. Otherwise we recommend modifying your project configuration as follows.

- Make sure you have `android:windowSoftInputMode="adjustResize"` in your `AndroidManifest.xml`:

  ```xml
  <activity
    android:name=".MainActivity"
    android:label="@string/app_name"
    android:windowSoftInputMode="adjustResize"
    android:configChanges="keyboard|keyboardHidden|orientation|screenSize">
  ```
  
If you use React Navigation, additional handling may be required to account for navigation headers and tabs. `KeyboardAvoidingView`'s `keyboardVerticalOffset` property can be set to the height of the navigation header and [`tabBarOptions.keyboardHidesTabBar`](https://reactnavigation.org/docs/en/bottom-tab-navigator.html#bottomtabnavigatorconfig) can be set to keep the tab bar from being shown when the keyboard is up. Due to a [bug with calculating height on Android phones with notches](facebook/react-native#23693), `KeyboardAvoidingView` is recommended over other solutions that involve calculating the height of the window.
  - adding an opaque background status bar on app.json (even though `android:windowSoftInputMode="adjustResize"` is set internally on Expo's Android apps, the transulcent status bar causes it not to work): https://docs.expo.io/versions/latest/guides/configuration.html#androidstatusbar


## Notes for local development

1. Install `yarn add -g expo-cli`
2. `expo start`

