# Privacy Policy

**FlexLex**
**Last Updated: July 2, 2026**

This Privacy Policy describes how FlexLex ("the App", "we", "us", or "our") handles information when you use our mobile application. By using the App, you agree to the practices described in this Privacy Policy. If you do not agree, please do not use the App.

## 1. Overview

FlexLex is a vocabulary learning application designed with a privacy-first approach. The App operates primarily offline. We do not collect, store, transmit, or sell your personal data to advertising networks, data brokers, or any third party, and we do not use analytics or tracking of any kind. All learning data you create — your sets, cards, images, progress and statistics — stays on your device unless you choose to export or share it.

The one exception is a non-personal device identifier used to verify FlexLex Pro purchases and to administer the free trial. This identifier is described in Section 5.1 and is the only data the App sends to and stores on a server we operate. It is never linked to your name, email, or your learning content.

## 2. Information We Do NOT Collect

- We do **not** collect personal information (name, email, phone number, address, etc.)
- We do **not** require user accounts, registration, or login
- We do **not** use analytics, tracking, or telemetry of any kind
- We do **not** use advertising SDKs or display ads
- We do **not** use cookies, device fingerprinting, or behavioral tracking
- We do **not** transmit crash reports or diagnostic data
- We do **not** access your contacts, call logs, SMS, location, microphone, or any sensor data beyond what is explicitly described below

## 3. Data Stored on Your Device

All data created within the App is stored locally on your device in a private application directory. This includes:

- **Study sets and folders** you create (names, languages, settings)
- **Flashcards** (words, translations, learning progress, spaced repetition data)
- **Card images** you add from your photo gallery
- **User preferences** (theme, font size, daily goals, streak data, haptics/sound settings)
- **Daily study statistics** (words studied and learned per day)
- **Spelling dictionaries** downloaded for offline spell-check

This data is not encrypted by the App beyond the default filesystem encryption provided by your device's operating system. If your device is compromised, this data could be accessible. We recommend keeping your device secured with a screen lock.

## 4. Camera and Photo Library Access

The App requests camera and photo library permissions solely for the following purposes:

- **Camera**: To scan printed text (e.g., textbook pages) using on-device optical character recognition (OCR) for importing words into your study sets. Photos taken for OCR are processed in memory and are not saved or retained by the App.
- **Photo Library**: To select images to attach to your flashcards for visual learning. Selected images are copied into the App's private storage. The App does not access, scan, index, or upload any other photos in your library.

You may deny these permissions; the App will continue to function without camera or photo features.

## 5. Network Usage and Third-Party Services

The App is designed to work offline. However, certain optional features require an internet connection. These features are always user-initiated and never occur in the background without your action.

### 5.1 Pro Purchase Verification and Free Trial (User-Initiated)

When you purchase or restore FlexLex Pro, redeem a promotional code, or start the free trial, the App communicates with our verification service hosted on Cloudflare Workers (`flexlex-pro.flexlexapp.workers.dev`). During this process, a device identifier (derived from your device hardware information) is sent to verify and bind your Pro entitlement — or your trial eligibility — to your device.

So that a Pro entitlement can be restored and so that the free trial can be offered once per device (and not repeatedly through reinstalling the App), this device identifier and the associated entitlement/trial status are **stored** on the verification service. This is the only user-related data we retain on a server. The identifier is a pseudonymous value; it is not linked to your name, email address, or any of your learning content, and it is never shared with or sold to any third party. The communication is encrypted in transit using TLS. See Section 9 for how to request deletion of this record.

### 5.2 Spell-Check Dictionaries (User-Initiated)

When you first use spell-check for a given language, the App downloads open-source Hunspell dictionary files from GitHub (`raw.githubusercontent.com`). These files are cached locally for offline use. No personal data is sent during this download.

### 5.3 Translation Suggestions (User-Initiated)

The App provides optional translation suggestions using on-device machine learning. The technology used depends on your platform:

- **Android**: The App uses Google ML Kit for on-device translation. When you download a translation model for a language, the model files (approximately 30 MB each) are downloaded from Google's servers. After download, all translations are performed entirely on your device. No text you translate is sent to Google or any external server. Google ML Kit SDKs may automatically collect device and app information, performance metrics, and diagnostic data for Google's internal analytics and product improvement purposes, even when translation is performed on-device. This data collection is governed by [Google's Privacy Policy](https://policies.google.com/privacy) and is not controlled by us. For details on what ML Kit collects, see [Google's ML Kit data disclosure documentation](https://developers.google.com/ml-kit/android-data-disclosure).

- **iOS**: The App uses Apple's built-in Translation framework (available on iOS 18.0 and later) for on-device translation. All translations are processed entirely on your device using Apple's system translation models. No text you translate is sent to any external server by the App. The Translation framework is provided and managed by Apple as part of iOS. For details on how Apple handles data, see [Apple's Privacy Policy](https://www.apple.com/legal/privacy/).

The set of supported translation languages may differ between platforms, as each relies on its respective provider's available language models. Translation suggestions are provided as a convenience and may not be available for all language pairs on all devices.

### 5.4 Text-to-Speech (Device Service)

The App uses your device's built-in text-to-speech (TTS) engine to pronounce words. Depending on your device and OS configuration, the TTS engine may use cloud services provided by your device manufacturer (e.g., Google, Apple). We do not control or have access to any data processed by your device's TTS service.

### 5.5 AI Story Generation (User-Initiated, On-Device)

The App includes an optional feature that generates short practice stories from the words in your study set using an on-device AI language model. All text generation happens locally on your device — the words in your set, your prompts, and the generated stories are **not** transmitted to us or to any external server.

The only network activity this feature involves is a one-time download of the AI model itself, which you explicitly trigger:

- On supported Android devices, the App may use the system's built-in on-device AI (Google AI Core / Gemini Nano), which is provided and managed by Google as part of your device.
- Otherwise, the App downloads an open-source language model (Qwen 2.5) from Hugging Face (`huggingface.co`). The model file is cached locally and reused for all future generations. No personal data or study content is sent during this download.

After the model is available, story generation works fully offline. This feature is optional; if you never open it, no model is downloaded.

## 6. Backup and Export

The App allows you to export your study sets and create full backups of your data. Exported files are saved in standard formats (.json, .zip) and shared via your device's native share sheet. Once you share or save a backup file, the security of that file is your responsibility. Backup files are not encrypted by the App.

**Automatic local backup after updates.** To protect your data across App updates, the first time you open the App after an update that changes its internal data format, the App automatically writes one backup file to your device's public **Downloads** folder (in a `FlexLex` subfolder). This file never leaves your device — it is written only to local device storage and is not uploaded anywhere. It is visible in your device's file manager so that you can restore or delete it yourself. Because it contains your complete study data, we recommend you treat it like any other backup file and delete it if you do not want it kept.

We strongly recommend storing backups in a secure location and not sharing them publicly, as they contain your complete study data.

## 7. Data Sharing

We do not share, sell, rent, trade, or otherwise disclose your learning content to any third party. The only way your study content leaves your device is if you manually export or share a study set or backup file. Certain optional, user-initiated features additionally make outbound connections that do **not** carry your learning content:

- Downloading spell-check dictionaries (connects to GitHub) or translation models (on Android, connects to Google)
- Downloading the optional AI story model (connects to Hugging Face; see Section 5.5)
- Verifying a Pro purchase or free trial (connects to our Cloudflare Worker and sends the non-personal device identifier described in Section 5.1)

The automatic post-update backup described in Section 6 is written only to your device's local Downloads folder and is never uploaded to us or anyone else.

## 8. Children's Privacy

The App does not knowingly collect any personal information from anyone, including children under the age of 13 (or the applicable age of digital consent in your jurisdiction). Since the App does not collect personal information, it does not require parental consent under the Children's Online Privacy Protection Act (COPPA), the General Data Protection Regulation (GDPR), or similar legislation. However, children should use the App under parental supervision, particularly when using features that require internet access.

## 9. Data Retention and Deletion

All your data is stored locally on your device. You have full control over it at all times.

- **Delete individual items**: You can delete any set, folder, or word within the App.
- **Delete all data**: You can wipe all App data at once via Settings → Data → Delete All Data within the App, or through your device's system settings (Settings > Apps > FlexLex > Clear Data).
- **Uninstalling the App** removes all locally stored data, including study sets, images, preferences, and statistics. Note that the automatic backup written to your public Downloads folder (Section 6) is **not** removed by uninstalling — you can delete it yourself from your device's file manager at any time.

The only data we retain off your device is the pseudonymous device identifier and associated Pro/trial status described in Section 5.1. This record contains no personal information and none of your learning content. If you would like this record deleted, contact us at the address in Section 16 and we will remove it; deleting it does not affect any data stored on your device.

## 10. Security

While we take reasonable steps to ensure data integrity within the App, we cannot guarantee the absolute security of data stored on your device. Security depends on your device's operating system, encryption settings, and physical security. We are not responsible for unauthorized access to your data resulting from device compromise, malware, or inadequate device security.

## 11. Third-Party Links and Services

The App may interact with third-party services as described in Section 5. We are not responsible for the privacy practices, content, or security of any third-party services, websites, or platforms. We encourage you to review the privacy policies of any third-party services you interact with through the App.

## 12. International Users

The App processes all data locally on your device. No data is transferred across borders by the App. If you use optional features that connect to third-party services (Google, GitHub), those services may process data in accordance with their own privacy policies and applicable laws.

## 13. Your Rights

Since we do not collect or store any personal data, traditional data subject rights (access, rectification, erasure, portability) under regulations such as GDPR, CCPA, or similar laws are exercised directly on your device through the App's built-in functionality (editing, deleting, exporting data).

## 14. Changes to This Privacy Policy

We may update this Privacy Policy from time to time. Any changes will be reflected by updating the "Last Updated" date at the top of this document. We encourage you to review this Privacy Policy periodically. Your continued use of the App after changes constitutes acceptance of the updated policy.

## 15. Disclaimer

THE APP IS PROVIDED ON AN "AS IS" AND "AS AVAILABLE" BASIS. WE MAKE NO WARRANTIES, EXPRESS OR IMPLIED, REGARDING THE ACCURACY, RELIABILITY, OR COMPLETENESS OF ANY TRANSLATIONS, OCR RESULTS, SPELL-CHECK SUGGESTIONS, OR OTHER CONTENT GENERATED BY THE APP OR THIRD-PARTY SERVICES USED WITHIN THE APP. USE OF THE APP AND ANY RELIANCE ON ITS OUTPUT IS AT YOUR OWN RISK.

## 16. Contact

If you have any questions, concerns, or requests regarding this Privacy Policy, please contact us at:

**Email:** privacy@flexlex.app

---

*This Privacy Policy applies to the FlexLex mobile application distributed via the Google Play Store and/or Apple App Store.*
