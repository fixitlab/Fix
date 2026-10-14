# FIX website + app (GitHub Pages package)

This package combines the public FIX introduction website and the existing FIX web app in one codebase. Visitors can read about FIX, then use Sign up or Log in to open the account form connected to the existing Supabase project.

## Publish on GitHub Pages
1. Create a new, empty GitHub repository.
2. Extract this ZIP on your computer.
3. Upload the **contents** of the extracted folder (index.html, app.js, styles.css, verify.html, and the assets folder) to the repository root. Do not upload the ZIP itself.
4. In GitHub, open **Settings → Pages** and publish from the `main` branch and `/ (root)`.
5. Wait for GitHub Pages to provide the published website address.
6. In Supabase, open **Authentication → URL Configuration**. Add the published website address and its `verify.html` URL to the allowed redirect URLs. Set the Site URL to the canonical published website address if this is now the primary website.
7. Test account creation, email confirmation, login, posting, profiles, follows, notifications, and messages with two test accounts.

## Important notes
- The package uses the existing Supabase URL and publishable key already present in the app. Do not replace these with a secret/service-role key.
- This is a static website; GitHub Pages does not run a private backend. Supabase remains the backend.
- The permanent top banner and the in-feed space are **placeholders**, not live ads. A real ad provider must approve the publisher/account and its approved ad code must be integrated before ads appear.
- The profile has a prominent “Get verified” button and blue-tick display support, but badge applications, payments, review, and issuance are not active yet. Do not collect payment-card information until a proper payment provider and verification workflow are implemented.
- No database SQL is required for this front-end update. Keep a backup of the previous working app before replacing it.
