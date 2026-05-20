# Privacy policy

_Last updated: 2026-05-20_

## 1. Who we are

`overtrain` is an Android app developed and published by an
independent developer. This policy describes how the app handles
data on your device. Questions about this policy can be sent to
**hi@overtrain.bike**.

## 2. What this policy covers

This policy applies to the `overtrain` Android application (package
`com.overtrain.app`) distributed through the Google Play Store. It
does not cover any third-party app you may choose to share your
workout files with after you export them yourself.

## 3. What the app stores on your device

`overtrain` reads data from Bluetooth Low Energy (BLE) sensors you
choose to pair with it and stores everything it records on your
device. Nothing is sent over the network — see §4.

The kinds of data the app handles are:

- **BLE sensor readings** — cycling power, cadence, and grade
  exchanged with your paired FTMS smart trainer; heart rate from an
  optional BLE heart-rate monitor; cadence from an optional BLE
  Cycling Speed and Cadence sensor.
- **Rider profile inputs** — values you enter in Settings such as
  FTP, body weight, bike weight, height, and either max heart rate
  or lactate threshold heart rate.
- **Workout history** — recorded samples from each ride so the
  History screen can render charts and stats.
- **Imported structured workouts** — any `.zwo` files you import
  through the system file picker.
- **Optional diagnostic logs** — when you turn on the verbose-logging
  toggle, the app writes small rotating log files so you can attach
  them to a bug report. They are shared only if you tap "Share logs".
- **Exported workout files** — at the end of each ride the app
  writes a Garmin `.fit` file into your device's `Documents/Workout/`
  folder so you can upload it to whichever service you prefer.

## 4. Data we do not collect

`overtrain` does **not** collect, transmit, or share any of the
following:

- No analytics of any kind.
- No crash reporting or telemetry.
- No advertising identifiers.
- No location data. The Android `BLUETOOTH_SCAN` permission is
  declared with the `neverForLocation` flag, which tells the system
  the app does not derive location from BLE scans.
- No user accounts, sign-up, or login.
- No remote servers, cloud sync, or back-end services.

The app does not declare the `INTERNET` permission in its Android
manifest. With that permission absent, the operating system prevents
the app from making any network requests at all.

## 5. Permissions and why each is requested

| Permission                                                     | Why it is requested                                                                                                                                                                                   |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `BLUETOOTH_SCAN` (`neverForLocation`)                          | Discover nearby smart trainers, heart-rate monitors, and cadence sensors when you tap "Scan" on the Pairing screen.                                                                                   |
| `BLUETOOTH_CONNECT`                                            | Open a Bluetooth Low Energy connection to a paired trainer, heart-rate monitor, or cadence sensor and exchange sensor / control data.                                                                 |
| `FOREGROUND_SERVICE` and `FOREGROUND_SERVICE_CONNECTED_DEVICE` | Keep the workout running and the Bluetooth connection alive while the screen is off or another app is in the foreground. The persistent notification is required by Android for this kind of service. |
| `POST_NOTIFICATIONS`                                           | Show the workout's foreground-service notification so Android does not kill it.                                                                                                                       |
| `WAKE_LOCK`                                                    | Prevent the device from suspending in the middle of a workout, which would interrupt sample recording and trainer control.                                                                            |

The app also declares `<uses-feature android:name="android.hardware.bluetooth_le"/>`
because Bluetooth Low Energy is required for the app to be useful.

## 6. Sharing with third parties

The app itself does not send any data to third parties.

If you tap a share button — for example, "Share FIT" on the History
detail screen, or "Share logs" on the Pairing screen's Diagnostics
row — Android's standard share-sheet opens and you choose which
other app receives the file (for example, Gmail, Drive, Strava,
Garmin Connect, or a messaging app). At that point the file is
governed by the receiving app's privacy policy, not this one. The
share is only initiated by an explicit tap from you.

## 7. Changes to this policy

If this policy changes in a way that affects how data is handled,
the "Last updated" date at the top of this page will be revised and
the new version will be published at the same URL. Material changes
will also be noted in the app's Play Store release notes.

## 8. Contact

Questions, concerns, or requests related to this policy can be sent
to **hi@overtrain.bike**.
