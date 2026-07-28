# Privacy Policy Brief — Animal Sounds & Ringtones (WildTones)

> **Purpose of this document**
> This file contains all the factual, technical information gathered directly from the app's source code. Feed it to an AI agent (e.g. ChatGPT, Claude, Gemini) with a prompt like: *"Using the facts below, write a clear and complete privacy policy web page for a Google Play app."* Then host the output on a simple static page and submit the URL in the Play Console.

---

## 1. App Identity

| Field | Value |
|---|---|
| **App name (Play Store / UI)** | Animal Sounds & Ringtones |
| **Branding / Splash name** | WildTones |
| **Tagline** | Animal Ringtones & Wallpapers |
| **Package name (Application ID)** | `com.animal.ringtones.sounds.wallpapers.high.quality.hd.amazing.app.download.now` |
| **Platform** | Android |
| **Minimum Android version** | Android 8.0 (API 26) |
| **Current version** | 1.0 |

> **TODO before publishing:** Fill in your developer/company name, contact email, and the live URL of the privacy policy page.

---

## 2. What the App Does (User-Facing Features)

- **Animal sounds & ringtones** — browse a catalog of animals (lion, wolf, elephant, macaw, cat, frog, and more) and listen to their sounds inside the app.
- **Wallpapers** — view high-quality animal wallpaper images organized by animal; some wallpapers are premium-only.
- **Favorites** — save animals to a local favorites list that persists between sessions.
- **Language selection** — choose from 7 interface languages (English, Spanish, French, German, Portuguese, Hindi, Arabic); preference is saved locally.
- **Premium subscription** — optional paid upgrade (Weekly / Yearly / Lifetime) that unlocks unlimited sounds, HD wallpapers, and removes ads; handled entirely through Google Play Billing.
- **Advertising** — free tier includes ads served by Google AdMob.

---

## 3. Data Collected Directly by the App

The app itself collects **no personally identifiable information**. The only data stored is:

### 3a. On-Device Preferences (SharedPreferences)
| Key | What it stores | Where |
|---|---|---|
| `onboarded` | Whether the user has completed first-run onboarding (true/false) | Device only |
| `lang` | The user's selected language code (e.g. "en", "es") | Device only |

- Not transmitted to any server.
- Deleted when the user clears app data or uninstalls.

### 3b. On-Device Favorites Database (SQLite)
| Column | What it stores | Where |
|---|---|---|
| `animal_id` | A text identifier for the favorited animal (e.g. "lion") | Device only |
| `created_at` | Timestamp of when it was added to favorites | Device only |

- Contains no personal information — animal IDs are fixed app content, not user-generated.
- Not transmitted to any server.
- Deleted when the user clears app data or uninstalls.

**The app has no user accounts, no sign-in, no email/phone collection, no forms, no user-generated content, and no custom backend.**

---

## 4. Data Collected by Third-Party SDKs

Although the app itself does not collect personal data, the following integrated third-party SDKs may collect data automatically as part of their normal operation.

### 4a. Google AdMob (Google Mobile Ads SDK)
- **Why it's integrated:** To display advertisements in the free tier.
- **What AdMob typically collects:** Advertising ID (GAID), IP address, device model, OS version, app usage signals, ad interaction data (clicks/impressions), coarse location derived from IP.
- **Purpose:** Showing relevant ads and measuring ad performance.
- **Governed by:** [Google's Privacy Policy](https://policies.google.com/privacy)

### 4b. Google UMP (User Messaging Platform)
- **Why it's integrated:** To show a consent dialog to users in the EEA, UK, and other applicable regions before personalised ads are served.
- **What it collects:** Consent choices (stored locally and reported to Google).
- **Governed by:** [Google's Privacy Policy](https://policies.google.com/privacy)

### 4c. Firebase Remote Config
- **Why it's integrated:** To allow remote configuration of app behaviour (e.g. feature flags) without a full app update.
- **What it collects:** App instance identifier, device/app metadata needed to deliver configuration.
- **Governed by:** [Google's Privacy Policy](https://policies.google.com/privacy)

### 4d. Google Play Billing
- **Why it's integrated:** To process premium subscription purchases (Weekly, Yearly, Lifetime).
- **What it handles:** Purchase tokens and subscription state. **The developer never receives or stores payment card data** — all payment processing is handled entirely by Google Play.
- **Governed by:** [Google Play Terms of Service](https://play.google.com/about/play-terms/)

### 4e. Glide (Image Loading)
- **Why it's integrated:** To load animal wallpaper images efficiently.
- **What it collects:** Nothing beyond standard HTTP requests to fetch image URLs; no tracking or analytics.
- **Open source:** [Glide on GitHub](https://github.com/bumptech/glide)

---

## 5. Permissions

The app requests the following permissions (several are added automatically by third-party SDK dependencies):

| Permission | Source | Purpose |
|---|---|---|
| `INTERNET` | SDKs | Required for ads, Firebase Remote Config, and Play Billing network calls |
| `ACCESS_NETWORK_STATE` | AdMob SDK | Check network connectivity before loading ads |
| `com.google.android.gms.permission.AD_ID` | AdMob SDK | Access Google Advertising ID for ad targeting/measurement |
| `ACCESS_ADSERVICES_TOPICS` | AdMob SDK | Android Privacy Sandbox: topic-based advertising |
| `ACCESS_ADSERVICES_AD_ID` | AdMob SDK | Android Privacy Sandbox: advertising ID |
| `ACCESS_ADSERVICES_ATTRIBUTION` | AdMob SDK | Android Privacy Sandbox: ad attribution/measurement |
| `READ_BASIC_PHONE_STATE` | Ads/Attribution SDK | Basic device state signal for ad fraud prevention |
| `com.android.vending.BILLING` | Play Billing SDK | In-app purchases and subscriptions |
| `WAKE_LOCK` | SDK component | Prevent CPU from sleeping during SDK operations |
| `FOREGROUND_SERVICE` | SDK component | Run foreground service for SDK background tasks |

**The app does NOT request:**
- Camera
- Microphone / Record Audio
- Contacts / Call Log
- Fine or Coarse Location
- Read/Write External Storage
- Any SMS/MMS permission

---

## 6. Network Communications

- The app's own code makes **no direct network requests** — there is no custom backend, API, or server.
- **All network traffic originates from third-party SDKs** listed in Section 4 (AdMob, Firebase, Play Billing).
- Future versions may load remote wallpaper images and audio files; this document will be updated if that changes.

---

## 7. In-App Purchases

- The app offers an optional **Premium upgrade** with three plans: Weekly, Yearly (best value), and Lifetime.
- All purchases are processed through **Google Play Billing**. The developer does not collect, store, or process any payment information.
- Premium features: unlimited access to all sounds, HD wallpapers, ad-free experience.
- Users can restore previous purchases using the in-app "Restore" option.

---

## 8. Advertising

- The free version of the app displays ads served by **Google AdMob**.
- Ads may be **personalised** based on your advertising ID and interests, subject to your consent choices (where a consent dialog is shown).
- Users in the EEA, UK, and other applicable regions will see a **consent dialog (UMP)** before personalised ads are shown. Users may choose non-personalised ads.
- Users can opt out of personalised ads at any time via Android device settings: **Settings → Privacy → Ads → Opt out of Ads Personalization**.
- Purchasing a Premium plan removes ads entirely.

---

## 9. Children's Privacy

- The app is designed for a **general audience** and is not directed at children under 13.
- The app does not knowingly collect personal information from children.
- If you believe a child has provided personal information through the app, please contact the developer (see Section 12) so appropriate action can be taken.

---

## 10. Data Retention

| Data | Retention |
|---|---|
| Local favorites (SQLite) | Stored on-device until the user clears app data or uninstalls |
| App preferences (SharedPreferences) | Stored on-device until the user clears app data or uninstalls |
| Ad-related data | Governed by Google's data retention policies |
| Firebase Remote Config data | Governed by Google's data retention policies |
| Purchase records | Governed by Google Play's policies |

---

## 11. Data Security

- The app stores user data only locally on the device; no custom server or cloud database is used.
- Local SQLite and SharedPreferences data are stored in the app's private internal storage, inaccessible to other apps.
- Android's Auto Backup is enabled. This means favorites and preferences **may be included in the user's Google account backup** (subject to the device's backup settings). This allows data to be restored if a user reinstalls the app.
- All third-party SDK network communications use HTTPS/TLS as provided by the respective SDK.

---

## 12. User Rights & Choices

Users can exercise the following controls at any time:

| Action | How |
|---|---|
| Delete favorites | Remove items from the Favorites screen inside the app |
| Change language | Open the Language screen in the app |
| Delete all local app data | Android Settings → Apps → Animal Sounds & Ringtones → Storage → Clear Data |
| Uninstall the app | Deletes all locally stored data |
| Opt out of ad personalisation | Android Settings → Privacy → Ads → Opt out of Ads Personalization |
| Manage consent (EEA/UK) | Via the in-app consent dialog (re-accessible from app settings, if applicable) |
| Restore purchases | Via the "Restore" option on the Premium screen |

---

## 13. Changes to This Privacy Policy

- The developer may update this policy when the app's data practices change (e.g. adding a backend, new SDKs, new features).
- The effective date at the top of the published policy page will be updated when changes are made.
- Continued use of the app after changes constitutes acceptance of the updated policy.

---

## 14. Developer Contact (TODO — fill in before publishing)

| Field | Value |
|---|---|
| **Developer / Company name** | *(your name or company name)* |
| **Contact email** | *(your support email)* |
| **Website / Support URL** | *(your website or Play Store listing URL)* |
| **Privacy policy page URL** | *(the URL you will submit to Play Console)* |

---

## Appendix A — Play Console "Data Safety" Form Guidance

Use this as a starting point when filling out the **Data Safety** section in the Play Console. Confirm against your live AdMob/Firebase configuration before submitting.

### Data collected or shared

| Data type | Collected | Shared | Required? | Encrypted | User can request deletion |
|---|---|---|---|---|---|
| **Device or other IDs** (Advertising ID) | Yes (by AdMob SDK) | Yes → Google & ad networks | No (ads can be disabled by going premium) | Yes (HTTPS) | Via device Ad ID reset |
| **App interactions** (ad clicks, impressions) | Yes (by AdMob SDK) | Yes → Google | No | Yes | N/A (SDK-level) |
| **App activity** (favorites list) | Yes (local only) | No | No | N/A (local) | Yes (clear data / uninstall) |
| **App info & performance** (diagnostics via Firebase) | Possibly (Firebase RC) | Yes → Google | No | Yes | Via Google account |
| **Financial info** (purchases) | By Google Play only | Google Play → developer (purchase token only) | No (optional premium) | Yes | Google Play policies apply |

### Data NOT collected
- Name, email address, phone number
- Address or precise location
- Photos, videos, audio files from the user
- Contacts or calendar
- Health/fitness data
- Browsing history outside the app

---

## Appendix B — Suggested AI Prompt

Copy and paste the following into an AI chat tool along with this entire document:

```
You are a legal writing assistant. Using only the facts provided in the document below, write a complete, user-friendly privacy policy web page for a Google Play Android app. The policy must:
- Be written in plain English, easy for a general audience to understand
- Cover all data practices mentioned in the document
- Include sections for: Introduction, Information We Collect, How We Use Information, Third-Party Services, Advertising, In-App Purchases, Children's Privacy, Data Security, Your Choices, Data Retention, Changes to This Policy, and Contact Us
- Use the placeholder text [DEVELOPER NAME], [CONTACT EMAIL], [WEBSITE URL], and [EFFECTIVE DATE] where the developer's details are needed
- Be formatted as clean HTML suitable for a simple static web page, or as Markdown

[paste the full contents of PRIVACY_POLICY_BRIEF.md here]
```
