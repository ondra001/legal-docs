# Privacy Policy

**FlexLex**
**Last Updated: August 2, 2026**

This Privacy Policy describes how FlexLex ("the App", "we", "us", or "our") handles information when you use our mobile application. By using the App, you agree to the practices described in this Privacy Policy. If you do not agree, please do not use the App.

## 1. Overview

FlexLex is a vocabulary learning application designed with a privacy-first approach. The App operates primarily offline. All learning data you create — your sets, cards, images, progress and statistics — stays on your device unless you choose to export or share it. We do not sell your personal data, and we do not use analytics or tracking of any kind for our own purposes.

There are three exceptions to the offline-by-default rule, each described in detail in Section 5:

- **Advertising.** The free version of the App displays ads supplied by Google AdMob. The AdMob SDK collects your device's advertising identifier and related device and usage data. This happens automatically while you use the free version — it is not something you initiate. See Section 5.6. FlexLex Pro removes all ads.
- **Pro purchase verification.** A non-personal device identifier is sent to and stored on a server we operate, solely to bind and restore your Pro entitlement. See Section 5.1.
- **AI Story generation (optional).** If you choose to enable this feature and supply your own Google Gemini API key, the words from your study set and your prompt are sent to Google's Gemini API. See Section 5.5.

Apart from these, we do not transmit your learning content anywhere.

## 2. Information We Do NOT Collect

- We do **not** collect personal information (name, email, phone number, address, etc.)
- We do **not** require user accounts, registration, or login
- We do **not** operate our own analytics, tracking, or telemetry
- We do **not** transmit crash reports or diagnostic data to ourselves
- We do **not** access your contacts, call logs, SMS, precise location, microphone, or any sensor data beyond what is explicitly described below
- We do **not** send your study sets, cards, images, or learning progress to our advertising partner, and your learning content is never used to target ads
- We do **not** sell or rent your data to data brokers

**Important:** the free version of the App does display third-party ads, and the Google AdMob SDK it uses collects your advertising identifier and certain device and usage data for its own purposes. That collection is described in Section 5.6 and is governed by Google's privacy policy, not ours. If you do not want it, FlexLex Pro removes ads entirely.

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

The App is designed to work offline. Most features that require an internet connection are optional and user-initiated. The one exception is advertising in the free version (Section 5.6), which loads automatically as you use the App.

### 5.1 Pro Purchase Verification (User-Initiated)

When you purchase or restore FlexLex Pro or redeem a promotional or gift code, the App communicates with our verification service hosted on Cloudflare Workers (`flexlex-pro.flexlexapp.workers.dev`). During this process, a device identifier (derived from your device hardware information) is sent to verify and bind your Pro entitlement to your device.

So that a Pro entitlement can be restored after a reinstall, this device identifier and the associated entitlement status are **stored** on the verification service. This is the only user-related data we retain on a server. The identifier is a pseudonymous value; it is not linked to your name, email address, or any of your learning content, and it is never shared with or sold to any third party. It is not used for advertising and is not shared with our advertising partner. The communication is encrypted in transit using TLS. See Section 9 for how to request deletion of this record.

### 5.2 Spell-Check Dictionaries (User-Initiated)

When you first use spell-check for a given language, the App downloads open-source Hunspell dictionary files from GitHub (`raw.githubusercontent.com`). These files are cached locally for offline use. No personal data is sent during this download.

### 5.3 Translation Suggestions (User-Initiated)

The App provides optional translation suggestions using on-device machine learning. The technology used depends on your platform:

- **Android**: The App uses Google ML Kit for on-device translation. When you download a translation model for a language, the model files (approximately 30 MB each) are downloaded from Google's servers. After download, all translations are performed entirely on your device. No text you translate is sent to Google or any external server. Google ML Kit SDKs may automatically collect device and app information, performance metrics, and diagnostic data for Google's internal analytics and product improvement purposes, even when translation is performed on-device. This data collection is governed by [Google's Privacy Policy](https://policies.google.com/privacy) and is not controlled by us. For details on what ML Kit collects, see [Google's ML Kit data disclosure documentation](https://developers.google.com/ml-kit/android-data-disclosure).

- **iOS**: The App uses Apple's built-in Translation framework (available on iOS 18.0 and later) for on-device translation. All translations are processed entirely on your device using Apple's system translation models. No text you translate is sent to any external server by the App. The Translation framework is provided and managed by Apple as part of iOS. For details on how Apple handles data, see [Apple's Privacy Policy](https://www.apple.com/legal/privacy/).

The set of supported translation languages may differ between platforms, as each relies on its respective provider's available language models. Translation suggestions are provided as a convenience and may not be available for all language pairs on all devices.

### 5.4 Text-to-Speech (Device Service)

The App uses your device's built-in text-to-speech (TTS) engine to pronounce words. Depending on your device and OS configuration, the TTS engine may use cloud services provided by your device manufacturer (e.g., Google, Apple). We do not control or have access to any data processed by your device's TTS service.

### 5.5 AI Story Generation (Optional, Uses Your Own Google Gemini API Key)

The App includes an optional feature that generates short practice stories from the words in your study set. This feature is **off by default** and does nothing until you supply your own Google Gemini API key, which you obtain directly from Google.

**If you enable it, your study content leaves your device.** When you generate a story, the App sends the words from the selected study set, together with the instructions for the story, to Google's Gemini API (`generativelanguage.googleapis.com`) using your API key. Google returns the generated story. This means:

- The words and translations in the set you generate from are transmitted to Google.
- The request is made under **your own** Google API key and is therefore subject to your own agreement with Google, including whatever quota, logging, retention and human-review practices apply to that key and account tier. We have no control over and no access to that data. See [Google's Gemini API Terms](https://ai.google.dev/gemini-api/terms) and [Google's Privacy Policy](https://policies.google.com/privacy).
- We do not receive, proxy, store, or see your prompts, your study content, or the generated stories. The App communicates with Google directly.

Your API key is stored on your device using the operating system's secure credential storage (Android Keystore / iOS Keychain). It is never transmitted to us. You can remove it at any time in Settings, which disables the feature.

If you never enter an API key, this feature makes no network requests and none of your study content is transmitted anywhere.

### 5.6 Advertising (Free Version Only)

The free version of the App is supported by advertising supplied by **Google AdMob**, a Google service. Ads appear in two places:

- A **banner** on browsing screens (such as your library and set details). Banners never appear during a study session.
- **Rewarded video ads** that you choose to watch in exchange for an in-app benefit, such as an extra heart, gems, or a spin of the Lucky Wheel. These only ever play when you tap to start them.

**FlexLex Pro removes all advertising**, and with it the AdMob data collection described below.

**What is collected.** To serve, cap, measure and (where permitted) personalise ads, the Google AdMob SDK collects information from your device. This typically includes:

- Your device's **advertising identifier** (the Android Advertising ID / Apple IDFA) — a resettable, pseudonymous ID used for ad personalisation, frequency capping and fraud prevention
- **Device and connection information** — device model, operating system version, language, country, screen characteristics, coarse network information and IP address (from which approximate, city-level location may be derived)
- **Ad interaction data** — which ads were requested, shown, viewed, or clicked, and diagnostic and performance information

This collection is performed by Google's SDK for Google's own purposes as an independent controller. **We do not receive this data**, we do not combine it with anything else in the App, and none of your study sets, cards, images, learning progress, or statistics are ever sent to Google for advertising. Google's handling of this data is governed by [Google's Privacy Policy](https://policies.google.com/privacy) and the [Google Advertising Privacy & Terms](https://policies.google.com/technologies/partner-sites). For details on how AdMob uses data, see [How Google uses information from sites or apps that use our services](https://policies.google.com/technologies/partner-sites).

**Your choices.**

- **Consent (EEA, UK, Switzerland).** On first launch in a region where it is required, the App shows a Google-certified consent message (Google's User Messaging Platform) before any ad loads, letting you accept or reject personalised advertising. Declining does not restrict your use of the App — you will simply see non-personalised ads. You can withdraw or change a previously given consent at any time by clearing the App's data (*Settings → Apps → FlexLex → Clear Data* on Android), which causes the consent message to be shown again on the next launch.
- **Reset or limit your advertising ID.** On Android: *Settings → Privacy → Ads*, where you can reset the ID or delete it entirely. On iOS: *Settings → Privacy & Security → Tracking*.
- **Remove ads entirely.** Purchase FlexLex Pro.

## 6. Backup and Export

The App allows you to export your study sets and create full backups of your data. Exported files are saved in standard formats (.json, .zip) and shared via your device's native share sheet. Once you share or save a backup file, the security of that file is your responsibility. Backup files are not encrypted by the App.

**Automatic local backup after updates.** To protect your data across App updates, the first time you open the App after an update that changes its internal data format, the App automatically writes one backup file to your device's public **Downloads** folder (in a `FlexLex` subfolder). This file never leaves your device — it is written only to local device storage and is not uploaded anywhere. It is visible in your device's file manager so that you can restore or delete it yourself. Because it contains your complete study data, we recommend you treat it like any other backup file and delete it if you do not want it kept.

We strongly recommend storing backups in a secure location and not sharing them publicly, as they contain your complete study data.

## 7. Data Sharing

We do not sell, rent, or trade your data. We do not disclose your learning content to any third party, with one exception you control: if you enable AI Story generation with your own Gemini API key, the study content you generate from is sent to Google (Section 5.5).

Your study content is **never** shared with our advertising partner and is never used to target ads.

Outbound connections the App makes, and what each carries:

| Feature | Connects to | Carries your learning content? |
|---|---|---|
| Advertising, free version (Section 5.6) | Google AdMob | No — but collects your advertising ID and device/usage data |
| AI Story generation, if enabled (Section 5.5) | Google Gemini API | **Yes** — the words in the selected set and your prompt |
| Pro purchase verification (Section 5.1) | Our Cloudflare Worker | No — only a pseudonymous device identifier |
| Spell-check dictionaries (Section 5.2) | GitHub | No |
| Translation models, Android (Section 5.3) | Google | No |
| Manual export or share | Wherever you send it | Yes — you choose the destination |

The automatic post-update backup described in Section 6 is written only to your device's local Downloads folder and is never uploaded to us or anyone else.

## 8. Children's Privacy

The App is intended for a general audience and is **not directed to children under 13** (or the applicable age of digital consent in your jurisdiction). We do not knowingly collect personal information from children.

Parents should be aware that the free version displays third-party ads and that the Google AdMob SDK collects the advertising identifier and device data described in Section 5.6. Where required, ads are served in non-personalised form for users identified as children or below the age of consent. The AI Story feature requires an adult to supply a Google API key and, once enabled, sends study content to Google (Section 5.5).

Children should use the App under parental supervision, particularly for features that require internet access. If you believe a child has provided personal information through the App, contact us at the address in Section 16.

## 9. Data Retention and Deletion

All your data is stored locally on your device. You have full control over it at all times.

- **Delete individual items**: You can delete any set, folder, or word within the App.
- **Delete all data**: You can wipe all App data at once via Settings → Data → Delete All Data within the App, or through your device's system settings (Settings > Apps > FlexLex > Clear Data).
- **Uninstalling the App** removes all locally stored data, including study sets, images, preferences, and statistics. Note that the automatic backup written to your public Downloads folder (Section 6) is **not** removed by uninstalling — you can delete it yourself from your device's file manager at any time.

The only data **we** retain off your device is the pseudonymous device identifier and associated Pro entitlement status described in Section 5.1. This record contains no personal information and none of your learning content. If you would like this record deleted, contact us at the address in Section 16 and we will remove it; deleting it does not affect any data stored on your device.

Data collected by **Google** — through AdMob (Section 5.6) or, if you enabled it, the Gemini API (Section 5.5) — is held by Google under its own retention policies and is not ours to delete. To exercise rights over that data, use Google's own controls (for advertising, reset or delete your advertising ID as described in Section 5.6; for the Gemini API, use the Google account that owns the API key).

## 10. Security

While we take reasonable steps to ensure data integrity within the App, we cannot guarantee the absolute security of data stored on your device. Security depends on your device's operating system, encryption settings, and physical security. We are not responsible for unauthorized access to your data resulting from device compromise, malware, or inadequate device security.

## 11. Third-Party Links and Services

The App may interact with third-party services as described in Section 5. We are not responsible for the privacy practices, content, or security of any third-party services, websites, or platforms. We encourage you to review the privacy policies of any third-party services you interact with through the App.

## 12. International Users

The App processes your learning content locally on your device. However, the third-party services described in Section 5 — in particular Google AdMob, which operates in the free version — may process and store data on servers outside your country, including in the United States. Those transfers are carried out by the respective provider under its own privacy policy, transfer mechanisms and applicable law, not by us. See [Google's Privacy Policy](https://policies.google.com/privacy) for details of Google's international transfers.

## 13. Your Rights

Because your learning content never leaves your device unless you send it somewhere, traditional data subject rights (access, rectification, erasure, portability) under regulations such as GDPR, CCPA and similar laws are exercised directly on your device through the App's built-in functionality (editing, deleting and exporting your data).

For the limited data that does leave your device:

- **The Pro entitlement record we hold** (Section 5.1) — request deletion at the address in Section 16.
- **Advertising data held by Google** (Section 5.6) — withdraw or change consent as described in Section 5.6, reset or delete your advertising identifier in your device settings, or purchase FlexLex Pro to stop ad serving altogether. Google is the controller for this data; requests concerning it should be directed to Google.
- **Gemini API data** (Section 5.5) — governed by the Google account that owns the API key you supplied. Remove the key in the App's settings to stop any further transmission.

We do not sell personal information, and we do not share it for cross-context behavioural advertising as those terms are defined under the CCPA/CPRA.

## 14. Changes to This Privacy Policy

We may update this Privacy Policy from time to time. Any changes will be reflected by updating the "Last Updated" date at the top of this document. We encourage you to review this Privacy Policy periodically. Your continued use of the App after changes constitutes acceptance of the updated policy.

## 15. Disclaimer

THE APP IS PROVIDED ON AN "AS IS" AND "AS AVAILABLE" BASIS. WE MAKE NO WARRANTIES, EXPRESS OR IMPLIED, REGARDING THE ACCURACY, RELIABILITY, OR COMPLETENESS OF ANY TRANSLATIONS, OCR RESULTS, SPELL-CHECK SUGGESTIONS, OR OTHER CONTENT GENERATED BY THE APP OR THIRD-PARTY SERVICES USED WITHIN THE APP. USE OF THE APP AND ANY RELIANCE ON ITS OUTPUT IS AT YOUR OWN RISK.

## 16. Contact

If you have any questions, concerns, or requests regarding this Privacy Policy, please contact us at:

**Email:** privacy@flexlex.app

---

*This Privacy Policy applies to the FlexLex mobile application distributed via the Google Play Store and/or Apple App Store.*
