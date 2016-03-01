

In order to run the live reloader, we have to start the react-native process.

```sh
$ react-native start --port 8082
```

Run a reverse proxy.  This allows debugging and live-reloading to work
correctly so the android can connect to the `react-native start` process.

```sh
$ sudo adb reverse --list
$ sudo adb reverse tcp:8082 tcp:8082
```

Install the app on the android device.

```sh
$ react-native run-android
```

Bring up the debug menu when the react app is actually running.
```sh
$ sudo adb shell input keyevent 82
```

After bringing up the debug menu, from the "Dev Settings" menu, input
"localhost:8082" as the dev server host and port.
