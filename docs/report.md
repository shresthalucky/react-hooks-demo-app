# Testing Ionic Native Features

[Ionic React](https://ionicframework.com/react) apps uses [Capacitor](https://capacitorjs.com/) project (Ionic's official native runtime) to unlock every native API across iOS, Android, Electron, and Web. However, [Ionic Native](https://ionicframework.com/docs/native) can also be used. They bridges the gap between WebView ([WebView](https://developer.android.com/reference/android/webkit/WebView) on Android and [UIWebView](https://developer.apple.com/documentation/uikit/uiwebview) on iOS) and Native API.

Installing capacitor if not installed:

```shell
npm i @capacitor/core
```

Instead of using [Capacitor Plugin APIs](https://capacitorjs.com/docs/apis) directly, [react-hooks](https://github.com/capacitor-community/react-hooks) provides access to Capacitor Plugin APIs, making it straightforward to use.

Installing react-hooks:

```shell
npm i @capacitor-community/react-hooks
```

This [blog post](https://ionicframework.com/blog/announcing-ionic-react-hooks/) talks about the announcing react hooks in Ionic.

## Tested APIs

### Storage

Available hooks to access [Storage API](https://capacitorjs.com/docs/apis/storage).

- ```useStorage```
- ```useStorageItem```

Q: Why use storage API instead of [localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage)?

A: As mentioned on storage API docs, "Mobile OS's may periodically clear data set in ```window.localStorage```, so this API should be used instead of ```window.localStorage```. This API will fall back to using ```localStorage``` when running as a Progressive Web App".

### Geolocation

Available hooks to access [Geolocation API](https://capacitorjs.com/docs/apis/geolocation).

- ```useCurrentPosition```
- ```useWatchPosition```

Accessing location of device is easy with hooks. The use of hooks is described well in its [docs](https://github.com/capacitor-community/react-hooks#geolocation-hooks).

## Pros of Ionic

- Ionic can be used with any web development frameworks
- Builds cross-platform hybrid apps
- Easy to start with rich pre-styled [UI components](https://ionicframework.com/docs/components)
- Ionic provides web UI with shared components, which assures consistency across devices
- [Debugging](https://ionicframework.com/docs/troubleshooting/debugging) is easy in Ionic

## Cons of Ionic

- Ionic is based on WebView wrapper - [WebView](https://developer.android.com/reference/android/webkit/WebView) on Android and [UIWebView](https://developer.apple.com/documentation/uikit/uiwebview) on iOS
- Ionic is not as performant as React Native when it comes to CPU usage, Battery consumption and UI rendering
- Need Cordova plugins or Capacitor plugins to access device's hardware functionality

## Links

- [https://www.simform.com/react-native-vs-ionic](https://www.simform.com/react-native-vs-ionic)
- [https://ionicframework.com/resources/articles/ionic-vs-react-native-a-comparison-guide](https://ionicframework.com/resources/articles/ionic-vs-react-native-a-comparison-guide)