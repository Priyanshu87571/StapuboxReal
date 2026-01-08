Stapubox OTP Login – React Native Assignment

This project is a 3-screen React Native Android application that implements mobile number login via OTP using the Stapubox APIs.

It follows the assignment requirements closely and is structured like a real production app.

🎯 Features Implemented
✅ Screen 1 – Send OTP

Indian mobile number input (10 digits)

Basic validation (starts with 6–9, length = 10)

Send OTP using Stapubox API

Loading state & error handling

Disabled button for invalid input

✅ Screen 2 – Verify OTP

4-digit OTP input boxes

Auto focus & auto move to next input

Auto-submit when all digits are filled

Resend OTP button with 60s cooldown timer

Error highlight on invalid OTP

"Change number" option to go back

API integration for:

Verify OTP

Resend OTP

✅ Screen 3 – Success

Simple success confirmation screen after login

✅ Android Behavior

Uses SMS Retriever API for automatic OTP reading (Android)

Graceful fallback to manual OTP entry if auto-read fails

🔌 API Integration

Base URL:

https://stapubox.com/trial


Endpoints used:

POST /sendOtp

POST /resendOtp

POST /verifyOtp

Authentication:

X-Api-Token: trial_XXXXXXXXXXXXXXXXXXXXXXXX


Token is configured in:
src/services/api.js

🗂️ Project Structure
StapuboxReal/
│── android/
│── ios/
│── src/
│   ├── navigation/
│   ├── screens/
│   ├── components/
│   ├── services/
│   ├── utils/
│   └── constants/
│
│── App.js
│── package.json
│── README.md

🛠️ Tech Stack

React Native CLI

React Navigation

Axios

Android SMS Retriever API

JavaScript

▶️ How to Run (On a machine with Android setup)
1. Install dependencies
npm install

2. Start Metro
npx react-native start

3. Run on Android (in new terminal)
npx react-native run-android


⚠️ Requires:

Java (JDK)

Android Studio

Android SDK

Emulator or real device

📦 Build APK
cd android
gradlew assembleRelease


APK output:

android/app/build/outputs/apk/release/app-release.apk

🧪 Testing Notes

OTP can be auto-read if SMS format supports SMS Retriever API

Manual OTP entry always works as fallback

Resend OTP is blocked for 60 seconds after each request

⚠️ Known Limitations

Android environment setup is required to run/build APK

Auto SMS read depends on SMS format provided by backend

Currently no persistent login session

🏆 Assignment Checklist

✅ Send OTP screen

✅ Verify OTP screen

✅ API integration (send, verify, resend)

✅ Auto OTP submit

✅ Validation errors

✅ Resend timer

✅ Android SMS auto-read

✅ Proper folder structure

✅ Ready for APK build

✅ GitHub repository

📌 Author

Priyanshu Raj
GitHub: https://github.com/Priyanshu87571
