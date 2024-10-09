# Language Translator App

This is an Android application that translates text from one language to another using Firebase ML Kit's Natural Language Translation API. The app allows users to select a source and target language, input text or use speech-to-text functionality, and receive the translated text.

## Features
- Translate text between multiple languages.
- Input text manually or use speech recognition to convert speech to text.
- Dynamic downloading of language models based on selected languages.
- Simple and clean UI with dropdowns for language selection and a button for translation.

## Prerequisites
Before you begin, ensure you have met the following requirements:
- Android Studio installed on your system.
- A Firebase project set up for the app, with ML Kit enabled.
- Google Firebase SDK added to your Android project.
- Internet connection to download translation models for the first use.

## Supported Languages
The app supports translation between the following languages:
- English
- Afrikaan
- Arabic
- Bengali
- Catalan
- Czech
- Hindi
- Urdu

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/language-translator-app.git
```
### 2. Setup Firebase
1. Go to the [Firebase Console](https://console.firebase.google.com/).
2. Create a new project or use an existing one.
3. Add your Android app to the Firebase project by following the setup steps.
4. Download the `google-services.json` file and place it in the `app/` directory of your Android project.

### 3. Add Dependencies
Ensure the following dependencies are added in your `build.gradle` (app) file:

```gradle
implementation 'com.google.firebase:firebase-ml-natural-language:22.0.1'
implementation 'com.google.firebase:firebase-ml-natural-language-translate-model:20.0.7'
implementation 'com.google.android.material:material:1.4.0'
```
## Code Overview

### `MainActivity.java`
The `MainActivity` handles the user interface and translation logic. It includes:
- Language selection through `Spinner` components.
- Speech-to-text input using the `RecognizerIntent`.
- Translation using Firebase's `FirebaseTranslator` for real-time language conversion.

### Key Methods
- `getLanguageCode()`: Maps language names to their respective Firebase language codes.
- `translateText()`: Downloads the required language models and performs the translation.

### FirebaseTranslatorOptions
Sets the source and target languages for translation:

```java
FirebaseTranslatorOptions options = new FirebaseTranslatorOptions.Builder()
        .setSourceLanguage(fromLanguageCode)
        .setTargetLanguage(tolanguageCode)
        .build();
```
# Screenshots
![WhatsApp Image 2023-06-27 at 10 44 49 PM](https://github.com/Pranavjaishwal/Language-Translator/assets/94792890/444dffc9-101c-4dbc-a2f1-47f71125a3dd)
![WhatsApp Image 2023-06-27 at 10 44 50 PM](https://github.com/Pranavjaishwal/Language-Translator/assets/94792890/832ae80b-a516-45c6-8911-e6e75779c1fc)


# Video Working Demo

https://github.com/Pranavjaishwal/Language-Translator/assets/94792890/80ec02d8-1c24-41f1-94f1-d7307d4b36b2

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributions
Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/your-username/language-translator-app/issues).

---

**Author:** P.Sri Harsha
**Repository:** [Language Translator App](https://github.com/your-username/language-translator-app)  


