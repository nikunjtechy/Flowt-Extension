# Privacy Policy for Flowt

*Effective date: November 12, 2026 (previous version: October 11, 2026)*
*Applies to: Flowt - Distraction Blocker for YouTube, version 1.1.0 and later*

This Privacy Policy explains how the Flowt browser extension ("Flowt", "the extension", "we", "us" or "our") handles information. It covers the extension itself and the support channels linked from it. Please read it together with the [Flowt License Agreement](https://nikunjtechy.github.io/Flowt-Extension/flowt-license).

## 1. Summary

- Flowt has **no servers, no accounts, no analytics, no advertising and no tracking**.
- Flowt **does not collect, transmit, sell or share** your personal information or your browsing or watch history. The extension makes no network requests of its own.
- Flowt's watch-time count is **a number of minutes per day, kept only on your device**. It never contains the titles, channels or addresses of the videos you watch, and it is never sent anywhere.
- Everything Flowt saves stays in your own browser, using the storage Chrome provides for extensions.
- The only time information reaches us is when **you choose** to email us or fill in the feature-request form.

## 2. Information Flowt stores on your device

Flowt stores only what it needs to work. None of this information is sent to us.

| Information | Where it is stored | Why |
|---|---|---|
| Feature settings (for example "Hide Home Feed", "Hide Comments" or "Hide Live Chat"), security options including Focus Lock and its wait length, break-reminder and daily-limit settings, the weekly schedules you create for Scheduled Blocking (their names, days, times and type), accent color, light or dark mode, and whether first-run setup has been completed | `chrome.storage.sync` | To remember your choices. If Chrome Sync is turned on, Chrome copies these settings to your other signed-in browsers. Choosing a Mode simply changes these same settings; the mode itself is not stored. |
| Your 4-digit PIN | `chrome.storage.local` (this device only) | To enforce the optional startup lock and the lock on changing settings. |
| Reasons you type before turning Flowt off (at most the 20 most recent, with the date and time) | `chrome.storage.local` (this device only) | Only used when you enable "Ask for a Reason Before Disabling", so you can review them on the settings page. |
| A breakage report: the names of Flowt features that appear to have stopped working on YouTube, with dates | `chrome.storage.local` (this device only) | To tell you in the popup when a YouTube change has broken a feature. It contains no page addresses or watch history. |
| Watch time: the total number of minutes a YouTube video was actually playing on each day, for the last 90 days | `chrome.storage.local` (this device only) | To show your watch time in the popup and to apply the optional break reminder and daily limit. It is a single number per calendar day. It contains **no video titles, channels, addresses or search terms**. Days older than 90 days are deleted automatically. |
| A running Focus Session: its start time, end time and which features it keeps hidden | `chrome.storage.local` (this device only) | To keep those features hidden until the session ends. Removed when the session ends. |
| A pending Focus Lock request: which switch you asked to turn off and when the wait ends | `chrome.storage.local` (this device only) | To make you wait, then confirm, before that switch turns off. Removed once you confirm, cancel, or the confirmation window passes. |
| The daily-limit allowance: the date and the YouTube video ID of the one video you were allowed to finish after reaching your daily limit | `chrome.storage.local` (this device only) | So that only that video can play on after your limit is reached. It holds a single entry, replaced the next time it is needed, and has no effect after that day. |
| Whether to offer the one-time Mode picker after installation | `chrome.storage.local` (this device only) | Removed as soon as you choose a Mode or skip the picker. |
| A temporary, one-time pass that allows a PIN reset | `chrome.storage.session` | Cleared automatically when the browser closes. |

**About the PIN.** The PIN is a self-control aid, not a security credential. It is stored on your device in readable form and is not encrypted. Anyone with access to your computer or browser profile could read it. **Do not reuse a PIN or code that protects anything else, such as a bank card or phone.**

**About Chrome Sync.** Chrome Sync is a Google service, not ours. When it is enabled, Google handles your synced settings under the [Google Privacy Policy](https://policies.google.com/privacy). Flowt never syncs your PIN, your reason log, the breakage report, your watch time, a running Focus Session, a Focus Lock request or the daily-limit allowance.

## 3. How Flowt works on YouTube

Flowt runs only on `https://www.youtube.com/*`. On those pages it reads the page structure, and the page data YouTube itself provides, **locally in your browser** to decide which elements to hide and which controls (such as autoplay) to switch off. This happens as the page loads and is never recorded, stored or sent anywhere. Flowt does not read your watch history, search history, comments, account details, cookies or passwords.

While Flowt is on, it also checks, locally, whether the video player on the page is playing. It adds the playing time to that day's total and nothing else: no titles, channels or addresses are kept. When your optional daily limit is reached, Flowt pauses the video on the page and shows its own notice. During a Scheduled Blocking slot you set to block YouTube, Flowt shows its own "YouTube is paused" page, which is bundled inside the extension and loads nothing from the internet.

## 4. Permissions and why they are needed

| Permission | Purpose |
|---|---|
| `storage` | Saves your settings, PIN, reason log, breakage report, watch time, Focus Session, Focus Lock request and daily-limit allowance in your browser, as described in Section 2. |
| `declarativeNetRequestWithHostAccess` | Powers two optional features. For "Permanently Block" Shorts, Flowt registers a single rule that sends `youtube.com/shorts` addresses to the YouTube home page. For Scheduled Blocking, during a slot you set to block YouTube, Flowt registers a single rule that shows its own "YouTube is paused" page instead of YouTube, and removes the rule when the slot ends. Chrome applies these rules itself; Flowt does not see, read or log your web requests. |
| `scripting` | When Flowt is installed or updated, it adds its own bundled scripts to YouTube tabs that are already open, so they work without a refresh. Flowt never loads or runs code from the internet. |
| `alarms` | Ends a Focus Session on time, and starts or ends a Scheduled Blocking slot on time. Flowt keeps at most one alarm for the end of a session and one for the next schedule change. Alarms carry no personal information. |
| Host access to `https://www.youtube.com/*` | Limits Flowt to YouTube. Within YouTube tabs it lets Flowt hide the elements you choose, count watch time locally and pause a video at your daily limit. It also lets Flowt find open YouTube tabs and send them to the right page when you turn on "Permanently Block" or when a Scheduled Blocking slot starts. These page addresses are checked at that moment and are never stored. |

Flowt cannot access any other website.

## 5. Information you choose to send us

We only receive information when you decide to send it:

- **Support email.** If you email [contact.flowt@gmail.com](mailto:contact.flowt@gmail.com), we receive your email address and whatever you include in the message.
- **"Report this" (breakage report).** If Flowt detects a problem and you click "Report this", your email app opens with a draft addressed to us. The draft contains the names of the affected features, the dates they were seen failing, your Flowt version and your browser's user-agent string (which identifies your browser and operating system version). **Nothing is sent unless you send the email yourself**, and you can edit or delete any part of it first.
- **"Request Feature".** This link opens a form hosted by Google Forms. We receive whatever you choose to enter. Google handles the form under its own privacy policy.

We use this information only to reply to you, investigate problems and improve Flowt. We do not sell it, use it for advertising, or share it with anyone except where the law requires us to. We keep support correspondence only as long as it is useful for those purposes, and you may ask us to delete it at any time.

## 6. Settings backup files

The settings page can export your settings to a file. The file is created in your browser and saved wherever you choose. It is never uploaded anywhere. The file contains your synced settings only, including any schedules you created. **Your PIN, reason log, breakage report and watch time are never included in a backup file.** You are responsible for keeping any exported file safe.

## 7. What we do not do

- We do not collect personally identifiable information through the extension.
- We do not use analytics, telemetry, crash reporting, cookies, fingerprinting or third-party tracking libraries.
- We do not sell, rent, trade or transfer user data to third parties.
- We do not use or transfer user data for purposes unrelated to Flowt's single purpose of reducing distractions on YouTube.
- We do not use or transfer user data to determine creditworthiness or for lending purposes.
- We do not keep a list of the videos you watch, the channels you visit or the things you search for.
- We do not run remote code.

## 8. About the focus and limit features

Focus Session, Focus Lock, the PIN, the reason prompt, the break reminder, the daily limit and Scheduled Blocking are **self-control aids that you choose to turn on**. They are not security, monitoring or parental-control tools, and they are not designed to stop someone who has full control of the browser, for example by uninstalling or disabling the extension. They work only in the browser where Flowt is installed and only on `https://www.youtube.com/*`. Watch time is an approximate count made on your device; it is not a medical, clinical or professional measure. Flowt never reports your watch time, your limits, your schedules or your reasons to anyone.

## 9. Chrome Web Store User Data Policy

Flowt's use of information complies with the [Chrome Web Store User Data Policy](https://developer.chrome.com/docs/webstore/program-policies/user-data-faq), including its Limited Use requirements.

## 10. Your control over your data

Because Flowt's data stays in your browser, you control it directly:

- **Reason log:** Settings → Accountability → *Clear Log*.
- **Breakage report:** *Dismiss* on the popup notice.
- **Schedules:** Settings → Scheduled Blocking → *Delete* on any schedule.
- **Watch time:** each day's total is deleted automatically after 90 days; uninstalling removes all of it at once.
- **Focus Session and Focus Lock:** removed automatically when the session or the wait ends. By design, a Focus Session cannot be ended early.
- **Appearance:** Settings → Customization → *Reset Customization*.
- **PIN:** Settings → Security & Access → *Reset PIN*.
- **Everything:** uninstalling Flowt removes the data Chrome stores for it on that device. Synced settings are governed by your Chrome Sync and Google Account settings.

For anything you have emailed us, write to [contact.flowt@gmail.com](mailto:contact.flowt@gmail.com) to access, correct or delete it.

## 11. Data security

Flowt relies on the storage Chrome isolates for each extension, and it limits itself to one website with the narrowest permissions that work. No method of storage is completely secure, though. Because we hold no user data on any server, there is nothing of yours on our side that could be breached.

## 12. Children's privacy

Flowt is a general-audience tool and is not directed at children under 13, or under the age of digital consent where you live. We do not knowingly collect personal information from children. If you believe a child has sent us personal information by email or through the form, contact us and we will delete it.

## 13. International users

Flowt is developed in India, and anyone can use it anywhere. Since the extension does not send personal information to us, it involves no cross-border transfer of user data. If you contact us, your message is handled by our email provider (Google) and may be processed outside your country. Where local data-protection laws give you rights (for example India's Digital Personal Data Protection Act, 2023, the EU/UK GDPR, or US state privacy laws), you may exercise them by contacting us. In most cases we will have no data about you to return.

## 14. Third-party services

Flowt links to services we do not control, including YouTube, Google Forms, Chrome Sync and your email provider. Their own privacy policies govern how they handle your information. Flowt only changes how YouTube pages look in your browser. Your use of YouTube itself remains subject to YouTube's and Google's terms and policies.

## 15. Changes to this policy

We may update this policy when Flowt changes. The updated version will be published at this address with a new effective date. If a change materially affects how information is handled, we will also mention it in the extension's release notes or store listing before or when it takes effect. Continuing to use Flowt after an update means you accept the revised policy.

## 16. Contact

Questions or requests about this policy: **[contact.flowt@gmail.com](mailto:contact.flowt@gmail.com)**
