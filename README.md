# 📱 React Native Voice Navigator

A React Native mobile app exploring core mobile development patterns — multi-level navigation, text-to-speech, audio playback, URL linking, and reusable component design. Built as a practical deep-dive into the React Native ecosystem.

---

## ✨ Features

- 🔐 **Authentication Flow** — login screen with form validation and toast feedback
- 🧭 **Multi-level Navigation** — Stack → Bottom Tabs → Drawer (all three navigation patterns in one app)
- 🔊 **Text-to-Speech** — converts user input to spoken audio via `react-native-tts`
- 🎵 **Audio Playback** — plays sound files using `react-native-sound`
- 🌐 **URL Linking** — opens URLs in the device's default browser
- ⚙️ **Background Tasks** — interval-based background execution demo
- 🧩 **Reusable Components** — `CustomTextInput` and `CustomButton` component library

---

## 🛠️ Tech Stack

![React Native](https://img.shields.io/badge/React_Native_0.76-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

| Library | Purpose |
|---------|---------|
| React Native 0.76.5 | Cross-platform mobile framework |
| React Navigation | Stack, Bottom Tab, and Drawer navigators |
| react-native-tts | Text-to-speech synthesis |
| react-native-sound | Audio file playback |
| react-native-reanimated | Gesture-driven animations |
| react-native-fast-image | Optimized image loading |
| react-native-toast-message | In-app toast notifications |
| react-native-permissions | Device permission management |
| react-native-vector-icons | MaterialIcons icon set |

---

## 🗂️ Navigation Architecture

```
StackNavigator
├── HelloWorldScreen       ← entry/splash
├── LoginScreen            ← auth (admin / admin)
└── Main → DrawerNavigator
              ├── Dashboard → BottomTabNavigator
              │               ├── HomeScreen   (TTS + audio + background task)
              │               └── WebScreen    (URL opener)
              └── Logout   ← navigates back to HelloWorld
```

---

## 📁 Project Structure

```
React-Native-Voice-Navigator/
├── src/
│   ├── screens/
│   │   ├── HelloWorldScreen.jsx   # Splash / entry screen
│   │   ├── LoginScreen.jsx        # Login with validation & toast
│   │   ├── HomeScreen.jsx         # TTS, audio, image background task
│   │   └── WebScreen.jsx          # URL input & deep linking
│   ├── navigation/
│   │   ├── StackNavigator.jsx     # Root stack
│   │   └── BottomTabNav.jsx       # Tabs + Drawer combined
│   ├── components/
│   │   ├── CustomTextInput.jsx    # Reusable input field
│   │   └── CustomButton.jsx       # Reusable button
│   └── assets/
│       ├── images/                # App images
│       └── sounds/                # Audio files
├── App.jsx
└── package.json
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- React Native CLI
- Android Studio (Android) or Xcode (iOS)

### Installation

```bash
# Clone the repository
git clone https://github.com/mbilalhussain15/React-Native-Voice-Navigator.git
cd React-Native-Voice-Navigator

# Install dependencies
npm install

# iOS only — install CocoaPods
cd ios && pod install && cd ..
```

### Run the App

```bash
# Android
npm run android

# iOS
npm run ios
```

### Login Credentials

```
Username: admin
Password: admin
```

---

## 📄 License

MIT © [Bilal Hussain](https://github.com/mbilalhussain15)
