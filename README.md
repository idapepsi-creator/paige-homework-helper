# Paige's Homework Helper

A free mobile-friendly web app for Paige and Amanda, using Firebase Authentication and Firestore.

## Upload to GitHub from iPhone
Upload **index.html**, **manifest.webmanifest**, and **icon.svg** (not the ZIP itself) to the root of the `paige-homework-helper` repository and commit.

## Deploy
GitHub Pages can host this app, but the repository must be public for free GitHub Pages on a Free personal account. **Never upload private student information or credentials to the repository.** Private homework data stays in Firestore protected by rules. In the repository, go to Settings → Pages → Deploy from branch → main / root → Save. Open the published site, enter Firebase web config from Firebase Console → Project settings → Your apps (create a Web app registration if needed), and sign in with Paige or Amanda's existing Firebase email/password account. In Firebase Authentication → Settings → Authorized domains, add the GitHub Pages domain if required. Safari → Share → Add to Home Screen.

## Important Firestore security rules
The earlier simple rules allowing both users to read/write `assignments` are functional but should be strengthened with field validation for production. The file `firestore.rules` provides a restricted version for the two existing Firebase user IDs. Publish it in Firestore → Rules before using the app. The app itself does not store passwords. Firebase config is public project identification, not a secret; do not put service account keys in files.

## Notes
- Both accounts can add/edit/delete, mark Finished or Turned In.
- 10 stars are awarded for a due-date-on-time turn-in. The star count is calculated from shared assignments.
- Overdue assignments are highlighted in the app (not push notifications).
- All assignments are shared between the two users.
- This starter app does not yet include push notifications, offline caching, or automatic parent email alerts.
