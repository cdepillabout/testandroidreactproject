

In order to run the live reloader, we have to start the react-native process.

```sh
$ react-native start
```

Run a reverse proxy.  This allows debugging and live-reloading to work
correctly so the android can connect to the `react-native start` process.

```sh
$ adb reverse --list
$ adb reverse tcp:8081 tcp:8081
```

Install the app on the android device.

```sh
$ react-native run-android
```

Bring up the debug menu when the react app is actually running.

```sh
$ adb shell input keyevent 82
```
