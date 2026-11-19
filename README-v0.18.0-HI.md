# SHRADDHA AI v0.18.0 — Unified Android Source

यह Android Studio source project है। इसे खोलने के लिए Android Studio (JDK 17), Android SDK Platform 35 और internet-connected Gradle sync चाहिए।

## इस ZIP में
- मूल SHRADDHA AI v0.17.0 unified project और पहले से मौजूद LIA/MYRA upstream source references
- नया Universal App Operator Training Lab
- Per-app semantic profiles और adaptive workflow runner
- Hindi voice command → trained workflow routing
- Authorized file locator + SAF folder grant + supported Android picker selection
- Risk/confirmation policy और metadata-only operator audit
- Hindi feature ledger, release notes और testing limitations

## Android Studio में खोलें
1. ZIP extract करें।
2. Android Studio → Open → extracted `SHRADDHA-AI-v0.17.0` folder चुनें।
3. JDK 17 और Android SDK Platform 35 स्थापित रखें।
4. Gradle Sync करें; Gradle wrapper 8.11.1 distribution internet से डाउनलोड हो सकती है।
5. Firebase इस्तेमाल करना हो तो `local.properties` में Firebase config values रखें या build environment variables सेट करें: `FIREBASE_API_KEY`, `FIREBASE_APP_ID`, `FIREBASE_PROJECT_ID`, `FIREBASE_SENDER_ID`, `FIREBASE_STORAGE_BUCKET`। Secrets को GitHub में commit न करें।
6. Debug APK: Android Studio Build → Build Bundle(s) / APK(s) → Build APK(s), या `./gradlew :app:assembleDebug`।

## Universal App Operator शुरू करें
1. ऐप खोलकर App Operator खोलें।
2. Android Settings में Shraddha Accessibility service को उपयोगकर्ता स्वयं ON करे। यह संवेदनशील अनुमति है।
3. जिस target app को train करना है उसे foreground में खोलें।
4. App Training / सीखने की लैब में वर्तमान स्क्रीन पहचानें, button/field का exact visible label या hint सहेजें, फिर workflow के steps जोड़ें।
5. Workflow save करें। अगली बार उसी target app को खोलकर Operator में बोले/लिखे गए निर्देश को saved workflow से match करें।
6. File upload के लिए File Access में Download/Pictures जैसे folder को Android system picker से एक बार grant करें। बाद में exact filename workflow step से खोजा जा सकता है।

## महत्वपूर्ण
यह build एक trained-workflow operator है, arbitrary third-party apps का guaranteed universal controller नहीं। हर ऐप के UI, Android version, picker, accessibility exposure और security restrictions अलग हैं। CAPTCHA, biometric prompts, secure fields, payment secrets, OTP/PIN/password और app की सुरक्षा को bypass नहीं किया जाता।

## Verification status
- ZIP structure और XML parsing जाँचे गए।
- Pure Kotlin learning/router/safety classes temporary platform stubs के साथ compile-check किए गए।
- Android Gradle build इस environment में पूरा नहीं हो सका: Gradle 8.11.1 distribution download पर `services.gradle.org` DNS/network unavailable था।
- APK install, Android emulator, real-device, OEM compatibility, Firebase sync और external app end-to-end tests अभी बाकी हैं। इस ZIP को compiled/tested APK नहीं कहा जा रहा।
