# ORIN Android starter project (v0.1)

This is a **native Android source-code starter**, not a prebuilt APK and not yet a full AI assistant. It is deliberately honest about its current limits.

## Implemented in this starter
- Native Android app screen with ORIN branding.
- On-demand speech input using Android's speech-recognition UI, after microphone permission.
- Spoken test responses using Android TextToSpeech (voice quality/language depend on installed Android voices).
- Optional notification access through Android's NotificationListenerService. The owner must enable access in Android Settings. The app shows captured notification title/text locally.
- A reply-draft field that reads the draft aloud; it does not send messages.

## Not implemented yet
- No AI model/API is connected; no intelligent summary or message classification yet.
- No automatic always-listening wake word. A reliable background wake word needs a dedicated, battery-conscious implementation and foreground-service/platform review.
- No sending replies, reading complete in-app message histories, placing/answering calls, or controlling other apps.
- No APK has been compiled or device-tested from this source.

## Build requirements
Open this folder in Android Studio on a computer, use JDK 17 and Android SDK platform 35, sync Gradle, then Build > Build APK(s). This project uses Android Gradle Plugin 8.7.3 and Kotlin 2.0.21. A compatible internet connection is needed to download Gradle dependencies. Review and test the source before installing.

## Important privacy notes
Notification access can expose private message previews. Enable it only if you understand that trade-off. This starter keeps captured notification text in app memory only and does not upload it. Do not add an AI service by putting a secret API key directly into an APK; use a secure backend and explicit consent before sending any private content to it.
