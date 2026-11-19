MAHA BILLING PWA - SOURCE PACKAGE

This is an installable web app (PWA), not a compiled Android APK.

Features: Firebase email/password signup and login; each signed-in user can access only their own Firestore records; GST and non-GST invoice calculations; customer and service/parts details; discounts; online bill history with open/delete; business details; print/save PDF from browser.

SETUP
1. In Firebase Authentication, enable Email/Password.
2. In Firestore Database > Rules, publish the rules in firestore.rules.
3. Host this folder on an HTTPS static host. Firebase Hosting is suitable, but its usual deployment flow uses Firebase CLI; another static host with Git integration can be managed from a phone.
4. In Firebase Authentication > Settings > Authorized domains, add the exact HTTPS hosting domain.
5. Open the hosted HTTPS URL in Chrome on Android, menu (three dots) > Install app or Add to Home screen.

SECURITY
Firebase web config is public client configuration, not a service-account private key. Do not publish service-account keys or share passwords. Firestore rules scope records to the authenticated user's UID. Use a strong password and secure your email account.

LIMITATIONS
Hosting is required; this package does not publish itself and does not compile an APK. Internet is required for login and cloud data. GST math is a simple percentage calculation; confirm tax rate, split CGST/SGST/IGST, and legal invoice requirements with your accountant. Backups are not configured.


WHATSAPP BILL SHARING
The WhatsApp bill details button opens the customer chat with a prefilled invoice summary. The user must review and tap Send. To send the PDF invoice, first use Print / Save PDF, save the PDF on the phone, then attach it in WhatsApp manually. The website cannot silently send messages or attach files without the user action.
