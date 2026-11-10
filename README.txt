N.G. PUBLIC SCHOOL — FIREBASE STARTER PACKAGE

FILES
- index.html: public school website; admission enquiries are saved to Firestore.
- admin.html: private admin sign-in and enquiry list.
- firestore.rules: restrictive Firestore security rules.

IMPORTANT PRIVACY / AUTHORIZATION
This is a technical starter, not permission to collect real student information.
Before using it with real families:
1. Get approval from the school owner/authorized administrator.
2. Have the school decide what student/guardian information is genuinely necessary.
3. Provide an appropriate privacy notice and obtain required parent/guardian consent.
4. Do not publish the admin page as a public link and do not share admin passwords.
5. Test first with fake/demo entries and delete test data afterward.

FIREBASE SETUP
1. Open Firebase Console and select project: ng-public-school-5b904.
2. Authentication > Sign-in method: ensure Email/Password is enabled.
3. Authentication > Users: create/confirm the administrator account.
4. IMPORTANT: The admin UID in admin.html and firestore.rules is currently set to:
   qOr1HZ9TyMN5piJjTD9nYoNqxth2
   Confirm this is the correct UID for the administrator account. If not, replace it in BOTH files.
5. Firestore Database > Rules: replace the rules with the contents of firestore.rules, then Publish.
6. Keep the Firestore database in production mode. Do not use open test rules.
7. Host index.html and admin.html on a proper HTTPS static host (Firebase Hosting or GitHub Pages).
8. Open index.html and submit a fake test enquiry.
9. Open admin.html and sign in with the administrator email/password. Confirm the test enquiry appears.

NOTES
- Firebase web config is intended to be included in a web app; Firestore Security Rules are what protect the data.
- Never put an administrator password in HTML or JavaScript.
- The current admin page permits read-only viewing in its interface; the rules reserve read/update/delete to the admin UID.
- This package uses Firebase JS SDK 10.12.2 from Google's CDN.
- If the school needs a production-grade system, add stronger abuse protection (such as App Check), audit/retention policy, and a server-side workflow.
