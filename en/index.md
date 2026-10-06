# Privacy Policy

**Last Updated: October 7, 2026**

This Privacy Policy explains how Monokura (the "App") collects, uses, and protects information when you use the App. "We", "us", and "our" refer to the developer of the App.

---

## 1. Information We Collect

### 1.1 Account Information

You can create an account using one of the following methods:

- **Google Account Login**: display name and email address
- **Apple Account Login**: display name and email address (including an Apple private relay address if you use Hide My Email)
- **Email and Password Registration**: display name and email address

This information is used for authentication through Firebase Authentication.

### 1.2 Data You Enter

The following data may be stored when you use the App:

- Board names, member information, and storage location names
- Shopping list, inventory, and rolling stock item information, including names, quantities, units, categories, and notes
- Purchase history, consumption history, and item change history
- Reminder location names, latitude, longitude, and notification radius
- Saved photos selected by Monokura Plus users and shared with members of the same board
- Recipe cover photos (available on Free) and recipe step photos (available on Monokura Plus), shared only with members of the same board

This data is stored in Google Firebase (Cloud Firestore for records and Cloud Storage for saved photo files) and shared with members of the same board.

### 1.3 Smart Input (Receipt Processing)

When you use Smart Input to create shopping or inventory suggestions from a receipt:

- On iOS, the preferred path uses Apple Vision OCR on the device and sends the extracted receipt text through our server to an AI inference service.
- If on-device OCR is unavailable or fails, a fallback may send the receipt image to the inference service.
- Monokura does not persist the receipt image as a saved photo, and operational logs do not record receipt text, receipt images, or model response bodies.
- Only rows that you review/edit and confirm are stored as normal shopping or inventory data. Content-free usage metadata may be stored for monthly quotas, rate limiting, and operational safeguards.

### 1.4 Location Information

If you enable location reminders, the App uses device location features to notify you when you are near a registered reminder location.

- Location information is used to provide the location reminder feature.
- Latitude and longitude registered as reminder locations are stored as shared board data.
- Location permission status and notification on/off settings are managed locally on each device.
- Notification messages include the location name and the fact that linked shopping items exist. Item names are not included in the notification body.

### 1.5 Purchase and Subscription Information

The App uses RevenueCat and App Store mechanisms to check the status of Monokura Plus purchases. We do not directly collect credit card numbers or other payment credentials. We may receive and store purchase status, product identifiers, expiration dates, and other information necessary to provide subscription features.

### 1.6 Automatically Collected Information

The App may automatically collect technical information through Firebase and related services, including:

- Device type and OS version
- App version, build number, and app language
- Feature usage information, excluding free-form item names, memo text, board IDs, and similar user-entered content
- Crash logs and error information to improve stability

### 1.7 In-App Support

When a signed-in user submits an in-app support request, we send the inquiry category and message body and, only when the user allows it, limited diagnostics such as app version, build number, platform, OS version, display language, and plan. Board IDs, inventory or recipe content, precise location, passwords, verification codes, and similar credentials are not sent as support diagnostics.

For in-app support, we do not store the raw Firebase UID as the support identity. Instead, an app-scoped pseudonymous identifier is used to associate support requests. This flow does not store the Firebase ID Token, real email address, or raw Firebase UID in ResolveHQ. Requests are routed through the Cloudflare-based Shared Support Platform and processed in ResolveHQ for customer support, troubleshooting, and operational protection.

### 1.8 Advertising and Tracking

The App currently does not display ads and does not perform advertising tracking.

---

## 2. How We Use Information

We use the collected information for the following purposes:

- Account authentication and security
- Providing shopping list, inventory, rolling stock, history, location reminder, and Smart Input features
- Sharing board data among board members
- Checking Monokura Plus purchase status and applying expanded limits
- Improving the App, analyzing usage, and fixing bugs
- Responding to user support inquiries

---

## 3. Sharing and Third-Party Services

We do not provide personal information to third parties except in the following cases:

- **Sharing with Board Members**: Members of the same board can view board item data, saved photos, history, reminder locations, display names, and related shared data.
- **Saved Photo Operations**: Board members may add saved photos and link them to items. Only the board owner or the user who uploaded a photo may delete it. Deleting a photo also removes its links from every item using it.
- **Service Providers**: The App uses the following third-party services. Please also refer to each service's privacy policy.
  - [Google Firebase](https://firebase.google.com/support/privacy) (authentication, data storage, app configuration, and usage analytics)
  - [RevenueCat](https://www.revenuecat.com/privacy/) (subscription management)
  - [Cloudflare](https://www.cloudflare.com/privacypolicy/) (AI inference path for Smart Input and intake/processing of in-app support through the Shared Support Platform)
  - [Apple](https://www.apple.com/legal/privacy/) (App Store payments, Sign in with Apple, notifications, location permission, and other OS features)
- **Legal Requests**: When disclosure is required by law or valid legal process.

---

## 4. Data Storage and Security

- Regular app data is stored on Google Firebase servers (Cloud Firestore for records and Cloud Storage for saved photo files). In-app support requests are processed and stored by the Cloudflare-based Shared Support Platform / ResolveHQ.
- Firebase security rules and Cloud Functions are used to restrict access to your own data and boards you participate in.
- Data transmission is encrypted using TLS.
- Because shared boards may contain sensitive notes, locations, or other personal content, please be careful about what you enter and share.

---

## 5. Data Retention and Deletion

- **Account Deletion**: After reauthentication, you can request account deletion from Settings. A retryable server-side job deletes and verifies related data, including photos on boards you own, before deleting the authentication account. Temporary failures are retried safely.
- **Subscriptions**: Deleting your account does not cancel App Store subscriptions. Please cancel subscriptions from your Apple Account subscription management screen.
- **History, prediction, and refill-waiting data**: Depending on App functionality and plan limits, data exceeding certain counts or retention periods may be deleted or trimmed.
- **Saved photos**: When Monokura Plus expires, photos are immediately hidden and cannot be selected. Photo files and metadata are retained for seven days after expiration and become visible again if Plus is restored during that period. If Plus remains inactive for seven days, the photo files in Cloud Storage, photo metadata in Cloud Firestore, and photo links on all items are deleted. Cloud Storage soft delete is configured for seven days for disaster recovery, so a recovery copy may remain for up to seven additional days after normal access is removed. Complete deletion may therefore take up to 14 days after Plus expires.
- **Inappropriate saved photos**: To report a photo, email the contact address below with the board name, information sufficient to identify the photo, and the reason for reporting. A board owner can remove a member from the board, and other members can leave the board. We review reports and may disable or delete content or take action on an account where appropriate.
- **Recipe photos**: Recipes and their cover/step photos are private board data. Cover photos are limited to one per recipe on Free; step photos require Plus. Recipes and their photos are shared board content and may be edited or deleted by board members. Deleting a recipe also deletes its recipe photos. Step photos are hidden immediately after Plus expires, retained for only seven days, and then deleted from Storage, metadata, and step references; restoring Plus during the grace period preserves them. Temporary recovery copies used during deletion are removed when processing completes. Cloud Storage soft delete may retain a disaster-recovery copy for up to seven additional days after normal access is removed, so complete deletion may take up to 14 days after Plus expires.
- **Smart Input**: Receipt images are not persisted as Monokura saved data. OCR text, or the image when fallback is required, is transmitted only as needed to generate the draft; only user-confirmed results are stored as normal shopping/inventory data. Content-free usage metadata may be retained for quotas, rate limiting, and operational safeguards.
- **In-App Support**: A support ticket with no activity for 30 days is automatically closed. The ticket body, messages, internal notes, and support-only pseudonymous customer data are deleted 30 days after close, so normal retention is up to about 60 days from the last support activity. Gateway idempotency data is retained for seven days, and rate-limit state is retained only for the minimum operational period (normally within one to seven days). Account deletion requests support-data erasure immediately rather than waiting for the normal retention window. Legal or security preservation is an exception only when required.
- **Guest Mode**: Guest board content such as item names, memo text, quantities, and locations is stored only in local storage on the device and is not sent to Firebase servers. We may separately collect low-cardinality Firebase Analytics events for app improvement and usage analysis, such as guest-mode starts, feature usage, and authentication-screen or authentication outcomes. These events do not include item names, memo text, board IDs, user IDs, or Firebase UIDs. Local guest data is automatically cleared when you log in.

---

## 6. Children's Privacy

The App is not intended for children under 13. We do not knowingly collect personal information from children under 13.

---

## 7. Changes to This Privacy Policy

This Privacy Policy may be updated as necessary. Significant changes will be notified in the App or on this page.

---

## 8. Contact

For questions about this Privacy Policy, please contact us at:

- **Email**: k.lifetime.app+monokura-support@gmail.com

---

*This Privacy Policy was originally created in Japanese.*
