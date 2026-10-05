# Privacy Policy — CDD Inventory

**Effective date:** 5 October 2026 (previous version: 24 July 2026)
**Apps:** CDD Inventory for Android (`com.cdd.inventory`) and for iOS / iPadOS (`com.cdd.inventory.ios`)
**Developer:** Matúš Drexler · matusdrexler@gmail.com

CDD Inventory is a laboratory inventory companion app (Android and iOS) for [CDD Vault](https://www.collaborativedrug.com/)
(Collaborative Drug Discovery, Inc.). It helps lab members find, check, and manage physical samples
stored in their own CDD Vault. This policy covers both the Android and the iOS app; where they
differ, the platform is named.

## The short version

The app does **not** collect, store, or share any personal data with the developer or anyone else.
There are no analytics, no advertising, and no tracking of any kind. Your data moves only between
your device and the CDD Vault servers of your own organization.

## Data the app handles

**CDD Vault API token.** To connect to your vault you enter an API token. It is stored on your
device only, in the operating system's protected storage — encrypted with an Android
Keystore–backed key on Android, and in the iOS Keychain (available only on this device, after its
first unlock) on iOS — and is sent exclusively to the CDD Vault server you configured, over HTTPS. It is never transmitted to the developer or any third
party, never written to logs, and never included in exports.

**Inventory data.** Samples, storage locations, plates, batches, molecules, and related records are
downloaded from your organization's CDD Vault and cached in a local database on your device so the
app works offline. This data stays on the device. Changes you make (for example depleting a sample,
moving it, or recording an inventory event) are written back only to your own CDD Vault, only when
you explicitly perform the action. How CDD processes that data is governed by your organization's
agreement with Collaborative Drug Discovery and the
[CDD privacy policy](https://www.collaborativedrug.com/privacy-policy).

**Inventory session records.** Scanning sessions and their reports (CSV/XLSX exports) are created
and stored locally. Sharing an export is always initiated by you, via the system share sheet
(Android or iOS), to a destination you choose.

## Camera

The camera is used for two things only: scanning barcodes/QR codes and on-device text recognition
(for example reading a CAS number off a label). All image processing happens **entirely on the
device**: on Android with Google ML Kit's on-device models, on iOS with Apple's built-in
AVFoundation barcode detection and Vision text recognition. Camera frames are analyzed in memory and
discarded — they are never stored, never uploaded, and never leave the device.

## Permissions

**Android**

- **Camera** — barcode scanning and on-device text recognition, as described above.
- **Internet** — communication with your configured CDD Vault server only.
- **Notifications / foreground service** — showing the progress of a running inventory sync.
- **Vibrate** — haptic feedback while scanning.

**iOS / iPadOS**

- **Camera** — barcode scanning and on-device text recognition, as described above. iOS asks for
  your consent the first time; you can withdraw it any time in Settings.
- Network access to your configured CDD Vault server only. The iOS app requests no other
  permissions (no location, contacts, photos, microphone or tracking).

## What the app does NOT do

- No analytics or crash-reporting SDKs.
- No advertising and no advertising identifiers.
- No account with the developer — the app has no backend of its own.
- No tracking across apps or websites (on iOS, the app never requests App Tracking Transparency).
- No sale or sharing of any data with third parties.

## Data deletion

All app data lives on your device. You can remove it at any time by deleting a vault profile in the
app (which also deletes its stored token and that vault's cached data), using *Clear local cache*
(Android), or simply uninstalling the app. On iOS, Keychain entries can outlive an uninstall; the
app deletes any token left over from a previous installation the first time it starts again. Data stored in your organization's CDD Vault is managed by your organization in CDD Vault
itself.

## Children

The app is a professional laboratory tool and is not directed at children under 13.

## Changes to this policy

If the app's data practices ever change, this document will be updated and the effective date
revised before the change ships.

## Contact

Questions about this policy: **matusdrexler@gmail.com**
