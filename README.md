<p align="center" >
<h3 align="center">
  💬 UY Chat
</h3>
<p align="center">
  The most complete chat UI for React Native
</p>


<p align="center">
  <img src="https://api.qrserver.com/v1/create-qr-code/?size=100x100&data=exp://expo.io/@xcarpentier/gifted-chat">
  <br>
  <a href="https://snack.expo.io/@xcarpentier/gifted-chat" target="_blank"><i>demo</i></a>
</p>

## Sponsor

<p align="center">
  <br/>
  <a href="https://www.lereacteur.io" target="_blank">
    <img src="https://raw.githubusercontent.com/FaridSafi/react-native-gifted-chat/sponsor-lereacteur/media/logo_sponsor.png">
  </a>
  <br>
  <p align="center">
    Coding Bootcamp in Paris co-founded by Farid Safi
  </p>
  <a href="https://www.lereacteur.io" target="_blank">
    <p align="center">
      Click to learn more
    </p>
  </a>
</p>

<p align="center">
  <br/>
  <a href="https://getstream.io/chat/?utm_source=github&utm_medium=react-native-gifted-chat&utm_campaign=sponsorship" target="_blank">
    <img src="https://i.imgur.com/oU7XYkk.png">
  </a>
  <br>
  <p align="center">
    Scalable <a href="https://getstream.io/chat/?utm_source=github&utm_medium=react-native-gifted-chat&utm_campaign=sponsorship" target="_blank">chat API/Server</a> written in Go
  </p>
  <p align="center">
    <a href="https://getstream.io/chat/get_started/?utm_source=github&utm_medium=react-native-gifted-chat&utm_campaign=sponsorship" target="_blank">API Tour</a> | <a href="https://dev.to/nickparsons/react-native-chat-with-chuck-norris-3h7m?utm_source=github&utm_medium=react-native-gifted-chat&utm_campaign=sponsorship" target="_blank">React Native Gifted tutorial</a>
  </p>
</p>

## Features

- _`react-native-web`able_ (ASAP: [#1284](https://github.com/FaridSafi/react-native-gifted-chat/pull/1284))
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

## Installation

- Using [npm](https://www.npmjs.com/#getting-started): `npm install react-native-gifted-chat --save`
- Using [Yarn](https://yarnpkg.com/): `yarn add react-native-gifted-chat`

## You have a question ?

1. Please check this readme and may find a response
1. Please ask on StackOverflow first: https://stackoverflow.com/questions/tagged/react-native-gifted-chat
1. Find response on existing issues
1. Try to keep issues for issues


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

- For **Expo**, there are at least 2 solutions to fix it:

  - Wrap GiftedChat in a [`KeyboardAvoidingView`](https://facebook.github.io/react-native/docs/keyboardavoidingview). This should only be done for Android, as `KeyboardAvoidingView` may conflict with the iOS keyboard avoidance already built into GiftedChat, e.g.:
```
<View style={{ flex: 1 }}>
   {
      Platform.OS === 'android' ?
         <KeyboardAvoidingView behavior="padding">
            <GiftedChat />
         </KeyboardAvoidingView> :
         <GiftedChat />
   }
</View>
```
If you use React Navigation, additional handling may be required to account for navigation headers and tabs. `KeyboardAvoidingView`'s `keyboardVerticalOffset` property can be set to the height of the navigation header and [`tabBarOptions.keyboardHidesTabBar`](https://reactnavigation.org/docs/en/bottom-tab-navigator.html#bottomtabnavigatorconfig) can be set to keep the tab bar from being shown when the keyboard is up. Due to a [bug with calculating height on Android phones with notches](facebook/react-native#23693), `KeyboardAvoidingView` is recommended over other solutions that involve calculating the height of the window.
  - adding an opaque background status bar on app.json (even though `android:windowSoftInputMode="adjustResize"` is set internally on Expo's Android apps, the transulcent status bar causes it not to work): https://docs.expo.io/versions/latest/guides/configuration.html#androidstatusbar

- If you plan to use `GiftedChat` inside a `Modal`, see [#200](https://github.com/FaridSafi/react-native-gifted-chat/issues/200).

## Notes for local development

1. Install `yarn add -g expo-cli`
2. `expo start`

