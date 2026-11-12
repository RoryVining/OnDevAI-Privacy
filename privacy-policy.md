---
title: Privacy Policy — OnDevAI
permalink: /privacy-policy/
---

# Privacy Policy — OnDevAI

**Effective date:** [EFFECTIVE DATE — to be filled in by the developer]
**App:** OnDevAI (Android package `com.ragdev.ai`)
**Developer / controller:** [DEVELOPER LEGAL NAME — to be filled in], [POSTAL ADDRESS — to be filled in], Australia
**Contact:** [CONTACT EMAIL — to be filled in]

## 1. Summary
OnDevAI runs artificial-intelligence models **on your device**. We (the developer) do **not** operate a server for the app, do **not** require an account, and do **not** receive your documents, chats, prompts, photos, generated images, voice recordings or files. The app has no advertising and no analytics or crash-reporting SDK from us.
The app does connect to the internet in a few situations (downloads, language packs, optional speech input). Those are described below so you know exactly what leaves your device.

## 2. Information stored on your device
The following stays in the app's private storage on your phone (it is not sent to us):
- **Documents you import** (PDF, TXT, Markdown, HTML, DOCX, XLSX, PPTX, images), their text chunks, extracted figures, and a search index built on-device with an embedding model.
- **Conversations** (your questions and the model's answers, with source references), your text-input history, and settings (theme, language, voice, alert preferences).
- **Downloaded or imported AI models**, voices and language packs.
- **Pictures you generate** or edit (stored in the app's gallery; if you tap Save, a copy is also written to your phone's Photos under *Pictures/RAGDev AI* (art) or *Pictures/RAGDev* (edited photos); if you tap Share, the file goes to the app you choose).
- **A Hugging Face access token, only if you choose to enter one** (to download gated models). It is encrypted with the Android Keystore and used only to authenticate to huggingface.co.
You can delete conversations, documents/index, models, voices and gallery images inside the app, and everything is removed when you uninstall (except pictures you saved to Photos, which you can delete there). Android's Auto Backup may copy some app data to your Google account if backup is enabled on your device.

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
The app lets you report an AI-generated answer or image as offensive. [DETAILS OF WHAT IS SENT, WHERE, AND FOR HOW LONG — to be filled in by the developer before release.] Reports are not linked to your identity because the app has no accounts.

## 6. Permissions
- **Camera** — to take a photo you attach to a chat or analyse; images stay on your device.
- **Microphone** — for voice input (see §4).
- **Notifications** — download progress and an optional "response ready" alert.
- **Vibrate** — optional haptic alert.
- **Foreground services** — keep a download you started running, and keep an image model loaded while you use other apps.
- **Internet** — §3.
Files are opened only through Android's file picker; the app does not request broad storage access.

## 7. Children
The app is not directed to children and is rated for adults. We do not knowingly collect information from children, and because we do not collect personal information this applies to all users.

## 8. Generated content
Answers and images are produced by AI models and may be inaccurate, offensive or inappropriate. Models and checkpoints you download or import are third-party works under their own licences (including use restrictions for Stable Diffusion/SDXL models). You are responsible for how you use outputs.

## 9. Your rights and choices
Because we hold no personal information about you, there is nothing for us to access, correct or delete on a server. You control your data on the device (see §2). To exercise rights under the Australian Privacy Act 1988 or other laws, or to ask a question, contact [CONTACT EMAIL — to be filled in]. You may complain to the Office of the Australian Information Commissioner (oaic.gov.au).

## 10. Security
Network requests use HTTPS. Your Hugging Face token (if any) is encrypted with the Android Keystore. Downloaded model files are checked against SHA-256 hashes where the app provides one.

## 11. Changes
We will post updates on this page with a new effective date. Material changes will also appear in the app's release notes.
