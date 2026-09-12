# Privacy Policy for Salah Window

**Last Updated:** September 13, 2026  
**Application:** Salah Window (`com.salahtracker`)  
**Developer:** Nabeel  
**Contact:** asharnabeel137@gmail.com  

---

### Overview

Salah Window is built from the ground up as a **100% offline, privacy-first application**. We believe your religious devotion, prayers, and personal reflections (*muḥāsabah*) belong strictly between you and your Creator. 

- **Zero Internet Access:** Salah Window does not request, declare, or possess the `android.permission.INTERNET` permission. It is technically impossible for the application to transmit your data across the internet.
- **Zero Third-Party SDKs:** The application does not contain any third-party advertising SDKs, tracking libraries, analytics frameworks, or cloud crash reporters.
- **Zero Account Creation:** No account, registration, login, phone number, or email is required to use the app.

---

### Permissions and Data Handling

#### 1. Location Data (`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`)
- **Purpose:** Location coordinates (latitude, longitude, and elevation) are used strictly on-device to calculate astronomical prayer times (Fajr, Shuruq, Dhuhr, Asr, Maghrib, Isha) and the Qibla compass bearing to Makkah.
- **Handling:** Location calculations occur entirely within local device code using offline astronomical algorithms. Location data is stored locally in the device's sandboxed storage and is **never transmitted off the device**. You may alternatively select a preset city or enter custom coordinates without granting GPS access.

#### 2. Alarms and Notifications (`USE_EXACT_ALARM`, `SCHEDULE_EXACT_ALARM`, `POST_NOTIFICATIONS`)
- **Purpose:** Exact alarms and local notifications are used strictly to alert you before prayer window deadlines expire and to deliver local prayer time reminders.
- **Handling:** All alarm scheduling and notifications are managed locally by Android's native `AlarmManager` and `NotificationManager`. No remote push notifications (FCM or APNs) are used.

#### 3. Local Storage and Backup
- **Purpose:** Your prayer logs, settings, and journal notes are stored locally in an on-device SQLite database (Room) and encrypted/sandboxed preferences (DataStore).
- **Handling:** If you choose to export a backup, the file is written directly to the local directory or cloud drive of your choice using Android's native Storage Access Framework (SAF). The app cannot access any other files on your device.

---

### Data Sharing and Disclosure

Because Salah Window operates entirely offline and does not collect or transmit personal data:
- We **do not sell, rent, trade, or share** any user data with third parties, advertisers, data brokers, or government agencies.
- We have no access to your logs, locations, streaks, or settings.

---

### Children's Privacy

Salah Window does not collect any personal information from anyone, including children under the age of 13.

---

### Changes to This Policy

If this Privacy Policy is updated, the changes will be posted in the project's public repository with an updated revision date. Because the app does not have internet access, any policy change will be bundled into app updates.

---

### Contact Us

If you have questions or suggestions about this Privacy Policy, please contact us at:
- **Email:** asharnabeel137@gmail.com
- **Public Repository:** https://github.com/m-d-nabeel/SalahWindow
