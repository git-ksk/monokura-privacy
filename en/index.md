# Privacy Policy

**Last Updated: July 17, 2026**

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

### 1.3 Location Information

If you enable location reminders, the App uses device location features to notify you when you are near a registered reminder location.

- Location information is used to provide the location reminder feature.
- Latitude and longitude registered as reminder locations are stored as shared board data.
- Location permission status and notification on/off settings are managed locally on each device.
- Notification messages include the location name and the fact that linked shopping items exist. Item names are not included in the notification body.

### 1.4 Purchase and Subscription Information

The App uses RevenueCat and App Store mechanisms to check the status of Monokura Plus purchases. We do not directly collect credit card numbers or other payment credentials. We may receive and store purchase status, product identifiers, expiration dates, and other information necessary to provide subscription features.

### 1.5 Automatically Collected Information

The App may automatically collect technical information through Firebase and related services, including:

- Device type and OS version
- App version, build number, and app language
- Feature usage information, excluding free-form item names, memo text, board IDs, and similar user-entered content
- Crash logs and error information to improve stability

### 1.6 Advertising and Tracking

The App currently does not display ads and does not perform advertising tracking.

---

## 2. How We Use Information

We use the collected information for the following purposes:

- Account authentication and security
- Providing shopping list, inventory, rolling stock, history, and location reminder features
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
  - [Apple](https://www.apple.com/legal/privacy/) (App Store payments, Sign in with Apple, notifications, location permission, and other OS features)
- **Legal Requests**: When disclosure is required by law or valid legal process.

---

## 4. Data Storage and Security

- User data is stored on Google Firebase servers (Cloud Firestore for records and Cloud Storage for saved photo files).
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
- **Recipe photos**: Recipes and their cover/step photos are private board data. Cover photos are limited to one per recipe on Free; step photos require Plus. Only the recipe creator or board owner may delete recipe photos. Deleting a recipe also deletes its recipe photos. Step photos are hidden immediately after Plus expires and deleted from Storage, metadata, and step references after seven days; restoring Plus during the grace period preserves them.
- **Guest Mode**: In guest mode, data is stored only in local storage on the device and is not sent to the server. Local data is automatically cleared when you log in.

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
