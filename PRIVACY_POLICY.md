# Privacy Policy — SmartRemind

**Last updated:** September 29, 2026  

**Package:** `com.smartreminddc.app`  

**Developer:** Denis Casian  

**Contact:** [support@rdcapps.com](mailto:support@rdcapps.com)  

**Website:** [deniscasian.com](https://deniscasian.com)  

**Privacy Policy:** [policy.rdcapps.com/smartremind.html](https://policy.rdcapps.com/smartremind.html)

SmartRemind ("the App", "we", "our") is a privacy-focused reminder and habit-tracking application developed by **Denis Casian**. This Privacy Policy explains how we collect, use, and protect information when you use our Android application. It is written in line with the principles of the EU GDPR, UK GDPR, and applicable US state privacy laws (including CCPA/CPRA and similar frameworks).

    
**Our promise:** SmartRemind stores all your reminders and habits **locally on your device**. We do not operate a server for this content and do not send reminder or habit content to advertising providers. The app contains Google AdMob advertising unless an eligible ad-removal purchase is active. Advertising and purchase services process the limited information described below.

## 1. Data we collect

All content you create — reminders, habits, history — is stored in a local SQLite database on your device (`smartremind.db`). This content is not sent to AdMob or RevenueCat. Third-party advertising and purchase services may process device, usage and purchase information as described in this policy.

    

| Data type | Where stored | Shared? |
| --- | --- | --- |
| Reminders (title, time, repeat) | On-device SQLite DB | Never |
| Habits (title, goal, progress) | On-device SQLite DB | Never |
| Trigger history | On-device SQLite DB | Never |
| App settings & preferences | On-device SharedPreferences | Never |
| Purchase status (Premium, Supporter, No Ads) | On-device cache and Google Play / RevenueCat | Purchase identifiers and entitlement status for verification |
| Advertising data and privacy choices | Google AdMob / User Messaging Platform and local consent state | Google and applicable advertising partners, subject to privacy choices and applicable law; no reminder or habit content |

## 2. Advertising & privacy choices

SmartRemind is supported by optional purchases and **Google AdMob** advertising. The app may display adaptive banners, native ads, interstitial ads and app-open ads. Premium Monthly and Premium Lifetime unlock features but **do not remove advertising**.

    
**What this means for you:** Your reminder and habit content stays on your device. AdMob may process an IP address (which can indicate approximate location), device or account identifiers such as the Android advertising ID where available, ad and app interactions, and diagnostic information for advertising, measurement and fraud prevention. Ad personalization and related processing depend on your privacy choices, regional requirements and the advertising configuration.

Google's **User Messaging Platform (UMP)** checks whether a privacy message is required before ads can be requested. Where required, the app presents the configured consent or privacy-choice form. You can revisit applicable choices through **Settings → Ad Privacy Choices** when that option is available. Declining personalization does not necessarily remove all advertising: non-personalized or limited ads may still be eligible under your choices and applicable requirements.

**Remove Ads / Supporter** (the one-time ad-removal purchase) removes all four ad formats while that entitlement remains valid. **Monthly Supporter** removes them while its subscription is active. Once an eligible entitlement is confirmed, the app disables advertising; it does not initialize the AdMob ads SDK at startup for users with confirmed ad-removal access. Ads may return if a purchase is refunded or revoked, or a subscription expires. The ad-privacy settings entry is hidden when ads are disabled.

## 3. Third-party services

### Google AdMob & User Messaging Platform — Advertising

Google Mobile Ads SDK serves advertising and processes advertising-related data. UMP manages consent and other applicable privacy choices. Their processing, storage periods and international transfers are governed by Google's policies and the applicable advertising partners' disclosures. We do not supply your reminder titles, descriptions, habit details or history to these services.

- [Google Privacy Policy](https://policies.google.com/privacy)

- [How Google uses information for advertising](https://policies.google.com/technologies/ads)

- [Google Mobile Ads SDK data disclosure](https://developers.google.com/admob/android/privacy/play-data-disclosure)

### RevenueCat — Purchases

SmartRemind uses **RevenueCat** to manage in-app purchases (No Ads, Monthly Supporter, Premium Monthly, Premium Lifetime). RevenueCat processes purchase tokens and subscription status but does **not** collect your personal reminder data.

    

- RevenueCat receives only anonymous purchase identifiers, not personal data;

- No reminder content, habit data, or personal information is sent to RevenueCat;

- [RevenueCat Privacy Policy](https://www.revenuecat.com/privacy/)

### Google Play Billing — Payments

All purchases are processed by **Google Play**. We receive only a purchase token to verify the purchase; no payment details are ever shared with us.

    

- Google Play handles all payment processing securely;

- [Google Privacy Policy](https://policies.google.com/privacy)

### ThreeTenABP — Date/time library

Used for date and time calculations. This is a local library — it makes no network requests and collects no data.

## 4. Premium features & purchases

SmartRemind offers optional premium features through in-app purchases:

    

- **Remove Ads / Supporter (No Ads)** — removes banner, native, interstitial and app-open ads (one-time purchase, subject to a valid entitlement);

- **Monthly Supporter** — removes all ads while active, plus Supporter badge and custom app icons (monthly subscription);

- **Premium Monthly** — unlimited reminders/habits, custom sounds, colours, priority levels (monthly subscription); **ads remain** unless you also have ad-removal access;

- **Premium Lifetime** — all premium features permanently, badge and icons (one-time purchase); **ads remain** unless you also have ad-removal access.

Purchases are processed by Google Play and managed by RevenueCat. We only receive anonymous purchase tokens to verify your entitlements. No payment information is shared with us.

    
**Free plan:** SmartRemind is fully functional without any purchases. You can create up to 5 reminders and 5 habits for free. Premium features unlock unlimited access and customisation options.

## 5. Alarm & notification system

SmartRemind uses Android's **AlarmManager** and **Notification** APIs to deliver reminders at the exact times you set, even when your device is in Doze mode or power-saving mode. The app implements a 3-layer safety system for maximum reliability:

    

- **Layer 1** — exact alarms using `setAlarmClock()` for maximum reliability;

- **Layer 2** — WorkManager backup system for additional safety;

- **Layer 3** — alarm chain that re-schedules all reminders every 30 minutes.

This ensures your reminders work consistently across all Android devices and manufacturers, including those with aggressive battery optimisation (Samsung, Xiaomi, Huawei, OnePlus, etc.).

    
**Visual confirmation:** When you set a reminder, a clock icon appears in your status bar confirming your alarm is active and scheduled to fire at the exact time.

    
**Notification content:** All notification content (title, description, emoji) is created entirely by you and stored only on your device. We never see or transmit your reminder content.

## 6. Permissions explained

    

| Permission | Why we need it |
| --- | --- |
| `POST_NOTIFICATIONS` | To show reminder notifications on Android 13+ |
| `SCHEDULE_EXACT_ALARM` / `USE_EXACT_ALARM` | To fire reminders at the exact time you set, even in Doze mode |
| `RECEIVE_BOOT_COMPLETED` | To restore scheduled alarms after device restart |
| `VIBRATE` | To vibrate the device when a reminder fires |
| `WAKE_LOCK` | To ensure the alarm wakes the device when needed |
| `INTERNET` | For purchase and subscription verification, UMP privacy messages and AdMob advertising |
| `ACCESS_NETWORK_STATE` | To check connectivity for purchases, privacy messages and advertising |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | To request exemption from battery optimisation so reminders fire reliably |

    
**Privacy note:** Reminder-related permissions support alarms and notifications. Network access also supports purchases and advertising. The Google Mobile Ads SDK may use the Android advertising ID where available and permitted. Reminder and habit content is not used for advertising.

## 7. Home screen widgets

SmartRemind provides two home screen widgets (Habits Widget and Smart Add Widget). These widgets read data from the local database on your device. No data is transmitted externally.

## 8. Data retention & deletion

Your reminders, habits and history are stored locally and remain on your device until you delete them. You can:

    

- delete individual reminders or habits from within the App;

- clear trigger history from the History screen;

- configure automatic history deletion (1, 3, 6, or 12 months) in Settings → History;

- uninstall the App to remove its local content (subject to any Android system backup).

    
**Note:** Because your reminder and habit content is stored locally, we cannot recover it after uninstallation. There is no cloud backup unless you use Android's system backup. Clearing app data does not automatically delete records already processed by Google, advertising partners or RevenueCat; their retention rules and privacy-request procedures apply to those records.

## 9. GDPR & data protection (EEA / UK / CH)

If you are located in the European Economic Area (EEA), United Kingdom, or Switzerland, you have the following rights under GDPR:

    

- **Right to Access** — you can request a copy of your data. Since all data is stored locally, you already have full access;

- **Right to Rectification** — you can edit or delete your reminders and habits directly in the app;

- **Right to Erasure** — you can delete all app data by uninstalling the app or clearing app data in device settings;

- **Right to Data Portability** — your data is stored in a standard SQLite database format on your device;

- **Right to Restrict Processing** — you can disable notifications or uninstall the app at any time.

We do not transmit reminder or habit content to our servers. For advertising-related processing, UMP presents applicable privacy choices and consent requests. You can withdraw or change applicable choices through Settings → Ad Privacy Choices when available. Contact us for privacy requests concerning the app, or consult the policies of Google, applicable advertising partners and RevenueCat for data they process. Where applicable, you may also lodge a complaint with your data-protection authority.

## 10. U.S. state privacy laws

If you are located in certain U.S. states (such as California, Virginia, Colorado, or Connecticut), you have additional rights:

    

- **Right to Know** — you can request information about app and third-party data processing described in this policy;

- **Right to Delete** — you can delete local app content and request deletion of applicable third-party records through the relevant provider;

- **Right to Opt-Out** — advertising-related disclosures may qualify as sharing or targeted advertising under applicable state laws. Use the applicable privacy choices to exercise available opt-out rights;

- **Right to Non-Discrimination** — we do not discriminate against users who exercise their privacy rights.

To delete local content, uninstall the app or clear app data in device settings. To exercise advertising-related choices, use Settings → Ad Privacy Choices when available. You can also contact us or the relevant third-party provider about applicable privacy rights.

## 11. Children's privacy

SmartRemind is not directed at children under 13 years of age. We do not knowingly collect personal information from children. If you believe a child has provided personal information through the App, please contact us so we can address this.

## 12. Security

Your reminder and habit content is protected by your device's security model — screen lock, encryption, etc. Advertising and purchase information may be processed outside your device by the services described above. We strongly recommend keeping your device software up to date.

## 13. Changes to this policy

We may update this Privacy Policy from time to time. When we do, we will update the "Last updated" date at the top of this page and, where appropriate, notify you through the App. Continued use of the App after changes constitutes your acceptance of the updated policy.

    

## 14. Contact us

If you have any questions or concerns about this Privacy Policy or the App's data practices, please contact us:

      
**Developer:** Denis Casian  

**Email:** [support@rdcapps.com](mailto:support@rdcapps.com)  

**Website:** [deniscasian.com](https://deniscasian.com)  

**Bug reports:** [bugs.rdcapps.com](https://bugs.rdcapps.com)  

**Privacy Policy:** [policy.rdcapps.com/smartremind.html](https://policy.rdcapps.com/smartremind.html)

©  Denis Casian — SmartRemind. All rights reserved.
