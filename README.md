# PRO-C126 - Alphabet Image Uploader (Expo)

A React Native (Expo) app that lets the user pick an image from the camera roll and upload it to a backend service for alphabet (handwriting) recognition.

## Features

- Image picker using **expo-image-picker** (editable, 4:3 crop, full quality)
- Requests **camera-roll permission** on non-web platforms
- Uploads the selected image as a **multipart/form-data** request to a `/predict-alphabet` endpoint (ngrok URL in the demo)
- Simple single-screen UI with one "Pick an image" button

## Tech Stack

- **React Native** / **Expo**
- **expo-image-picker** and **expo-permissions**

## Project Structure

```
├── App.js                 # Root component (renders PickImage screen)
├── screens/camera.js      # Image picking + multipart upload logic
├── app.json               # Expo app configuration
└── assets/                # App icons and splash screen
```

## Installation

1. Clone the repository.
2. Install dependencies:

```bash
npm install
```

## Usage

```bash
npm start          # or: npx expo start
npm run android    # Android
npm run ios        # iOS
```

1. Grant camera-roll permission when prompted.
2. Tap **Pick an image from camera roll** and select a photo.
3. The image is uploaded to the configured `/predict-alphabet` endpoint; the JSON result is logged to the console.

> Note: the demo upload URL is a temporary ngrok tunnel — replace it with your own model-serving endpoint.
