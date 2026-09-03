# Family Expense — Android v1 starter

This is a native Android project scaffold for the Family Expense app.

Implemented:
- Android 16 / API 36 target
- Local SQLite expense database
- SMS transaction detection using READ_SMS / RECEIVE_SMS
- Notification listener transaction detection
- Basic transaction parsing for INR/UPI/bank-style debit messages
- Confirmation before an automatically detected transaction is saved
- Manual expense entry
- Local Wi-Fi server scaffold for family synchronization

Important:
- The SMS and notification features require the user to explicitly grant Android permissions.
- The Wi-Fi sync layer is intentionally a secure-development scaffold, not production-ready cryptography/sync yet.
- Before Play Store release, add encrypted authenticated sync, family pairing, conflict resolution, privacy policy, Data Safety declarations, and a proper first-run consent/disclosure flow.
- Google Play currently lists SMS-based money management as a permitted SMS use case, but SMS access remains restricted and subject to Play review and declaration.
- Build with Android Studio or an Android-compatible build environment. This repository does not include the Gradle wrapper binaries.

Next build milestones:
1. Family pairing QR/code over LAN.
2. Encrypted authenticated device-to-device sync.
3. Expense split engine and balances.
4. Bank/UPI parser library with editable rules.
5. Categories and monthly analytics.
6. Export/backup.
7. Production Play Store privacy/permissions flow.


## Phone-only build

This project includes `.github/workflows/build-apk.yml`. You can upload the project to a GitHub repository from a phone browser, then use GitHub Actions -> Build Family Expense APK -> run workflow. The resulting `app-debug.apk` is available as an Actions artifact for download and installation on an Android test device.

This workflow creates a debug APK for testing. A Play Store release requires a signed release build/AAB and completion of Google's policy, data-safety, and permissions declarations.
