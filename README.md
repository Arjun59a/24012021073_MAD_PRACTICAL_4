# Alarm Scheduler Android App

<div align="center">
  <img src="app/src/main/res/drawable/alarm.jpeg" alt="Alarm app preview" width="220" />
</div>

<p align="center">
  <img alt="Kotlin" src="https://img.shields.io/badge/Kotlin-100%25-7F52FF?style=for-the-badge&logo=kotlin" />
  <img alt="Android" src="https://img.shields.io/badge/Android-API%2031%2B-3DDC84?style=for-the-badge&logo=android" />
  <img alt="Material" src="https://img.shields.io/badge/Material-Design-757575?style=for-the-badge&logo=materialdesign" />
</p>

A clean Android application built in Kotlin for scheduling precise alarms, showing the selected time on the home screen, and playing a ringtone when the alarm triggers. The app also supports canceling scheduled alarms through a dedicated broadcast flow.

## Features

- Set an exact alarm time using a TimePicker
- Schedule alarms with Android AlarmManager and PendingIntent
- Start and stop alarm playback using a custom service
- Show active alarm details in the app UI
- Cancel an alarm from the app
- Request exact alarm permission on supported Android devices
- Material UI card-based layout for a modern Android experience

## App Flow

1. User taps the Create Alarm button.
2. A time picker opens and the user chooses the alarm time.
3. The selected time is displayed on the screen.
4. A broadcast receiver triggers the alarm service at the scheduled time.
5. The ringtone starts playing.
6. The user can cancel the alarm manually from the app.

## Screenshots

### Main screen

<img src="https://github.com/user-attachments/assets/0ed00836-e04a-417d-a75e-67533febfb1c" width="300" alt="Main screen" />

### Time selection

<img src="https://github.com/user-attachments/assets/f4384e5c-41a2-496b-a0f0-5ccdb905f8b6" width="300" alt="Time picker" />

### Alarm scheduled on home UI

<img src="https://github.com/user-attachments/assets/b3fb6cc8-6278-4f01-9354-02019a7d8d09" width="300" alt="Alarm scheduled" />

## Project Structure

```text
24012021073_MAD_PRACTICAL_4/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/a24012021073_mad_practical_4/
│   │   │   │   ├── MainActivity.kt
│   │   │   │   ├── AlarmBroadcastReceiver.kt
│   │   │   │   └── AlarmService.kt
│   │   │   ├── res/
│   │   │   │   ├── drawable/
│   │   │   │   ├── layout/
│   │   │   │   ├── raw/
│   │   │   │   └── values/
│   │   │   └── AndroidManifest.xml
│   │   └── ...
│   └── build.gradle.kts
├── build.gradle.kts
├── gradlew
├── gradlew.bat
├── settings.gradle.kts
├── gradle.properties
├── README.md
└── .gitignore
```

## Core Components

### MainActivity
Responsible for:
- launching the time picker
- storing the scheduled alarm time
- showing the alarm in the UI
- creating the start and stop PendingIntent actions

### AlarmBroadcastReceiver
Handles the system broadcast and decides whether to:
- start the alarm service
- stop the alarm service

### AlarmService
Plays the ringtone using MediaPlayer and keeps the alarm sound active until stopped.

## Tech Stack

- Kotlin
- Android SDK
- Material Components
- AlarmManager
- PendingIntent
- BroadcastReceiver
- MediaPlayer

## Setup and Run

### Requirements

- Android Studio
- JDK 11 or newer
- Android SDK
- Emulator or physical Android device

### Steps

1. Clone the repository:

```bash
git clone https://github.com/Arjun59a/24012021073_MAD_PRACTICAL_4.git
```

2. Open the project in Android Studio.

3. Let Gradle sync and download the required dependencies.

4. Run the app on an emulator or physical device.

5. When prompted, allow the app to schedule exact alarms.

## Notes

This project is designed as a learning-focused Android practical, demonstrating real-world alarm scheduling behavior using Android's system services and broadcast-based event handling.

## Repository Details

- Repository: Arjun59a/24012021073_MAD_PRACTICAL_4
- Language: Kotlin
- Platform: Android

---

Made with ❤️ for Android alarm scheduling practice.
