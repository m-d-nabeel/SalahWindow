# Privacy Policy for Salah Window

**Last Updated:** November 21, 2026  
**Application:** Salah Window (`com.salahtracker`)  
**Developer:** Nabeel  
**Contact:** [GitHub Issues](https://github.com/m-d-nabeel/SalahWindow/issues)  

---

### Overview

Salah Window works entirely on your phone. Your prayers, notes and reflections (*muḥāsabah*) never leave it unless you choose to save a backup somewhere else.

- **No internet access.** The app does not request, declare or hold the `android.permission.INTERNET` permission, so it cannot connect to the internet. Prayer times, the Qibla direction and place names are all worked out on the phone.
- **No advertising, tracking or analytics.** The app contains no advertising SDKs, tracking libraries, analytics frameworks or crash reporters. Besides Android's own (AndroidX) libraries, it uses two third-party libraries — `adhan2` (prayer time astronomy) and Haze (a visual blur effect) — and a list of place names from GeoNames bundled into the app. None of them send anything anywhere.
- **No account.** No registration, login, phone number or email is needed.

---

### What the app uses, and why

#### 1. Location (`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`)
- **Purpose:** your latitude and longitude, to calculate prayer times and the Qibla direction.
- **When:** only when you tap *Detect current location*. The app never reads your location in the background and does not request background location. You can search for a place or enter coordinates instead of granting the permission at all.
- **Precise or approximate — your choice:** Android lets you pick either when it asks. Both work. Precise lets the app use GPS when there is no Wi-Fi or mobile signal (for example outdoors without data); approximate relies on Wi-Fi or mobile signal.
- **Kept to about 1 km:** whichever you choose, the app rounds the position to about 1 km before keeping it — that moves a prayer time by a second or two, and your stored settings and backups never hold your exact spot.
- **Handling:** Android's own location service works out the position under your phone's location settings. The app stores the rounded coordinates and the name of your place in its private storage on your phone and never transmits them.
- **Place names:** searching for a town, and naming the place you detected, use a list of towns bundled in the app (GeoNames, [geonames.org](https://www.geonames.org), CC BY 4.0). The lookup happens on the phone; nothing is sent.
- **Qibla compass:** the compass reads your phone's orientation sensors on the phone. No permission is needed and nothing is sent.

#### 2. Alarms and notifications (`USE_EXACT_ALARM`, `SCHEDULE_EXACT_ALARM`, `POST_NOTIFICATIONS`, `VIBRATE`)
- **Purpose:** to alert you at the start of a prayer's time, before it ends, and when it has ended, at the exact minute. `SCHEDULE_EXACT_ALARM` is declared only for Android 12 and earlier; newer versions use `USE_EXACT_ALARM`. `VIBRATE` lets an alarm vibrate.
- **Handling:** alarms and notifications are scheduled on the phone by Android's `AlarmManager` and `NotificationManager`. No push notifications or servers are involved.

#### 3. Keeping alarms working (`RECEIVE_BOOT_COMPLETED`, `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_SHORT_SERVICE`, `WAKE_LOCK`)
- **Purpose:** `RECEIVE_BOOT_COMPLETED` re-schedules your prayer alarms after the phone restarts. The short foreground service plays an alarm's sound while it rings. `WAKE_LOCK` comes with AndroidX WorkManager, which re-checks your alarms in the background, and keeps the phone awake for the moment that check needs.
- **Handling:** none of these read or send personal data.

#### 4. Your records, backups and files
- **Storage:** your prayer logs, notes, reflections and settings are kept in the app's private storage on your phone (a Room database and DataStore preferences). They are sandboxed — other apps cannot read them — but not separately encrypted.
- **Android system backup is off.** `android:allowBackup` is `false`, and the backup rules exclude everything from both cloud backup and phone-to-phone transfer, so Android does not copy your records off the phone.
- **Backups you make:** you can export a backup file, or turn on automatic backups, to a folder you choose with Android's file picker. The app writes only to that folder. If you pick a folder that a cloud service syncs (such as Google Drive), that service uploads the file under its own terms — this is the only way your records can leave the phone, and only if you choose it.
- **Files you pick:** the app reads a file only when you choose it — a backup to restore, or an audio file to use as your alarm sound. It cannot see any other files on your phone.

---

### Sharing

The app does not collect or transmit any personal data, so:
- We **do not sell, rent, trade or share** any data with third parties, advertisers, data brokers or governments.
- We have no access to your logs, locations, reflections or settings.

---

### Deleting your data

Everything the app keeps is on your phone. Clearing the app's storage, or uninstalling it, deletes it. Backup files you exported stay wherever you saved them until you delete them.

---

### Children's privacy

Salah Window does not collect personal information from anyone, including children under 13.

---

### Changes to this policy

Changes are published in the project's public repository with a new date above. Because the app has no internet access, it cannot notify you of changes; updates arrive with new versions of the app.

---

### Contact

Questions or suggestions about this policy:
- **Issues:** [github.com/m-d-nabeel/SalahWindow/issues](https://github.com/m-d-nabeel/SalahWindow/issues)
- **Repository:** [github.com/m-d-nabeel/SalahWindow](https://github.com/m-d-nabeel/SalahWindow)
