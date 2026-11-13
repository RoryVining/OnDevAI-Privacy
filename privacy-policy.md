---
title: Privacy Policy — OnDevAI
permalink: /privacy-policy/
---

# Privacy Policy — OnDevAI

**Effective date:** 14 November 2026
**App:** OnDevAI (Android package `com.ondevai.app`)
**Developer / controller:** FastcommData Solutions, QLD, Australia
**Contact:** romega_x@orica.com

## 1. Summary
OnDevAI runs artificial-intelligence models **on your device**. We (the developer) do **not** operate a server for the app, do **not** require an account, and do **not** receive your documents, chats, prompts, photos, generated images, voice recordings or files. The app has no advertising and no analytics or crash-reporting SDK from us.
The app does connect to the internet in a few situations (downloads, language packs, optional speech input). Those are described below so you know exactly what leaves your device.

## 2. Information stored on your device
The following stays in the app's private storage on your phone (it is not sent to us):
- **Documents you import** (PDF, TXT, Markdown, HTML, DOCX, XLSX, PPTX, images), their text chunks, extracted figures, and a search index built on-device with an embedding model.
- **Conversations** (your questions and the model's answers, with source references), your text-input history, and settings (theme, language, voice, alert preferences).
- **Downloaded or imported AI models**, voices and language packs.
- **Pictures you generate** or edit (stored in the app's gallery; if you tap Save, a copy is also written to your phone's Photos under *Pictures/OnDevAI* (art) or *Pictures/RAGDev* (edited photos); if you tap Share, the file goes to the app you choose).
- **A Hugging Face access token, only if you choose to enter one** (to download gated models). It is encrypted with the Android Keystore and used only to authenticate to huggingface.co.
You can delete conversations, documents/index, models, voices and gallery images inside the app, and everything is removed when you uninstall (except pictures you saved to Photos, which you can delete there). The app's data is not included in Android backups (the app turns Android Auto Backup off).

## 3. When the app uses the internet

<table>
<thead><tr><th>Situation</th><th>Who we connect to</th><th>What is sent</th></tr></thead>
<tbody>
<tr><td>Opening the app: refreshing the list of downloadable models</td><td>GitHub (<code>raw.githubusercontent.com</code>)</td><td>A normal web request (your IP address and app identifier "OnDevAI"); no personal data and no content</td></tr>
<tr><td>You download a chat model, image model or voice</td><td>Hugging Face (<code>huggingface.co</code> and its content-delivery hosts), GitHub Releases (<code>github.com</code>, voices)</td><td>A normal web request (IP address, "OnDevAI" user-agent, and your Hugging Face token to huggingface.co <strong>only if</strong> you entered one)</td></tr>
<tr><td>You paste your own model download link</td><td>The host you chose</td><td>A normal web request</td></tr>
<tr><td>You download translation or language-ID packs</td><td>Google (ML Kit)</td><td>Handled by Google's ML Kit service; see §4</td></tr>
</tbody>
</table>
Those services receive your IP address and technical request data and handle it under their own privacy policies (Hugging Face, GitHub, Google). We do not control or receive it.

## 4. Third-party components
- **Google ML Kit** (translation, language identification, text recognition): processing of your text happens on the device. The ML Kit SDK may send limited technical and usage diagnostics to Google (such as device and app information, identifiers, performance metrics, the languages used, and error codes). See https://developers.google.com/ml-kit/android-data-disclosure and Google's privacy policy.
- **Speech input**: when you tap the microphone, the app asks Android's speech recogniser to transcribe. If an on-device recogniser is available the app asks for it; **if it fails, the app may retry using the online recogniser provided by your device (usually Google)**, which then receives the audio under its own privacy policy. The app does not store the recording.
- **Text-to-speech**: offline voices run on-device (Piper voices via sherpa-onnx); otherwise your phone's text-to-speech service is used.
- **AI models** (e.g. Qwen, DeepSeek-R1 distill, Phi-4-mini, Gemma, Stable Diffusion, FLUX) run entirely on the device after download.
We use no advertising, analytics or crash-reporting SDK.

## 5. Reporting offensive AI content
The app lets you report an AI-generated answer or image as offensive. When you tap Report, the app saves the report (the reason you pick, an optional note, the prompt, the generated output, the model name and the app version) **on your device only**. Nothing is sent to us or anyone else automatically. You can view, share or export the saved reports from Settings → Reported content; if you choose to share one, it goes to the app you pick in Android's share menu. If you want us to see a report, email it to romega_x@orica.com. Reports are not linked to your identity because the app has no accounts. Delete saved reports in the app at any time.

## 6. App permissions and what they're for
These are the permissions the app declares. The app does not ask for contacts, location, phone, SMS, calendar, or access to all your files or photos. Documents and images reach the app only through Android's file and photo pickers, which you control.

**Permissions Android asks you about while you use the app (you can say no):**

| Permission | What it allows | Where it is used | If you deny it |
|---|---|---|---|
| Camera | Taking a photo with the camera | When you tap the camera button to attach a photo to a chat, use live camera, or use the camera screen. Photos stay on your device (see §2). | You cannot take a photo; you can still choose an existing picture from your gallery. |
| Microphone | Recording your voice while you speak | When you tap the microphone for voice input (see §4). Only while you are using it; the app does not store the recording. | Voice input does not work; typing still works. |
| Notifications (Android 13 and newer) | Showing notifications | Download progress, and the optional "response ready" alert (Settings). Asked when you start a download or turn that alert on. | No notifications are shown; downloads and responses still work. |

**Permissions that are granted automatically when you install (Android does not ask you):**

| Permission | What it allows | Where it is used |
|---|---|---|
| Internet | Connecting to the internet | Downloading models, voices and language packs, and refreshing the list of downloadable models when you open the app (§3). If you are offline, those fail, but models and documents already on your device keep working. |
| Network state | Checking whether you are connected | Used by the download and language-pack libraries to check for a connection before starting a download. |
| Foreground service, and foreground service for data sync | Keeping a task running with a visible notification while you use other apps | Keeps a model, voice or language-pack download running when you leave the app. |
| Wake lock | Keeping the phone awake briefly for background work | Used by Android's background-work library (WorkManager) while a download is running. |
| Receive boot completed | Letting background work resume after the phone restarts | Used by the same background-work library for queued downloads. |
| Vibrate | Vibrating the phone | Only if you turn on the optional "Vibrate" alert in Settings (off by default). |

**Only on Android 9 and older:**

| Permission | What it allows | Where it is used | If it is not granted |
|---|---|---|---|
| Write external storage | Saving files to shared storage | Saving a picture you choose to save into your Photos. It is declared for Android 9 and older only; newer Android versions do not need it. | Saving to Photos may not work on those versions; sharing still works. |

You can review or change runtime permissions at any time in your phone's Settings → Apps → OnDevAI → Permissions.

## 7. Children
The app is not directed to children and is rated for adults. We do not knowingly collect information from children, and because we do not collect personal information this applies to all users.

## 8. Generated content
Answers and images are produced by AI models and may be inaccurate, offensive or inappropriate. Models and checkpoints you download or import are third-party works under their own licences (including use restrictions for Stable Diffusion/SDXL models). You are responsible for how you use outputs.

## 9. Your rights and choices
Because we hold no personal information about you, there is nothing for us to access, correct or delete on a server. You control your data on the device (see §2). To exercise rights under the Australian Privacy Act 1988 or other laws, or to ask a question, contact romega_x@orica.com. You may complain to the Office of the Australian Information Commissioner (oaic.gov.au).

## 10. Security
Network requests use HTTPS. Your Hugging Face token (if any) is encrypted with the Android Keystore. Downloaded model files are checked against SHA-256 hashes where the app provides one.

## 11. Changes
We will post updates on this page with a new effective date. Material changes will also appear in the app's release notes.
