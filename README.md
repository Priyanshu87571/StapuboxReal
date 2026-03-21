# Stapubox OTP Authentication – React Native (Android)

A production-style mobile authentication flow built with React Native implementing OTP-based login using the Stapubox APIs.
The project focuses on clean architecture, UX polish, and real-world mobile engineering practices.

📸 Preview


✨ Key Highlights

📱 Modern 3-screen authentication flow

🔢 4-digit OTP with auto-focus & auto-submit

⏱ Resend OTP with 60s cooldown timer

🤖 Automatic OTP reading using Android SMS Retriever API

🛡 Robust validation & error handling

🧱 Scalable, production-style folder structure

⚡ Optimized UX with loading states & disabled actions

📦 Ready for APK release build

🧭 User Flow

Enter Mobile Number

Indian number validation (10 digits, starts with 6–9)

Calls Send OTP API

Verify OTP

Auto-focus inputs

Auto-submit when filled

Auto-read SMS on supported devices

Resend OTP with timer

Error highlighting on failure

Success Screen

Confirms successful authentication

🔌 API Integration

All APIs are integrated as per assignment spec.

Base URL

https://stapubox.com/trial


Endpoints

POST /sendOtp

POST /resendOtp

POST /verifyOtp

Auth Header

X-Api-Token: trial_XXXXXXXX


Configured in:

src/services/api.js

🏗️ Project Architecture

StapuboxReal/

│── android/

│── ios/

│── src/

# App navigation
│   ├── navigation/

# Screen-level components
│   ├── screens/

 # Reusable UI components
│   ├── components/
# Reusable UI components
│   ├── services/
# API layer
│   ├── utils/
# Helpers (validation, timer)
│   └── constants/
# Theme & constants
│── App.js

│── package.json

│── README.md


This structure is designed to scale cleanly in real production apps.

🛠️ Tech Stack

React Native CLI

React Navigation

Axios

Android SMS Retriever API

JavaScript

▶️ Running the Project

Requires Android development environment (Java, Android Studio, SDK, Emulator or device).

npm install
npx react-native start
# In new terminal
npx react-native run-android

📦 Building Release APK
cd android
gradlew assembleRelease


Output:

android/app/build/outputs/apk/release/app-release.apk

🧪 Quality & UX Considerations

Disabled actions during API calls

Clear loading indicators

Graceful error states

Fallback to manual OTP if auto-read fails

Defensive input validation

Clean separation of concerns (UI / logic / API)

⚠️ Known Limitations

Auto OTP reading depends on SMS format from backend

No persistent login session implemented (by design, out of scope)

✅ Assignment Coverage
Requirement	Status

Send OTP screen	✅

Verify OTP screen	✅

API integration	✅

Auto OTP submit	✅

Resend OTP timer	✅

Validation highlighting	✅

SMS auto-read	✅

Modular architecture	✅

APK ready	✅

GitHub repo	✅

🧠 Engineering Decisions

React Native CLI chosen for full native API access (SMS Retriever)

Service layer abstraction for API calls

Reusable OTP input component

Separation of concerns for maintainability and testing

👤 Author

Priyanshu Raj
GitHub: https://github.com/Priyanshu87571
