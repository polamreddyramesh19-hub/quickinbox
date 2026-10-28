# QuickInbox — personal temporary email client

This is a small PWA website that uses the public Mail.tm API to create a temporary inbox and read received messages. It does not send email and does not provide its own email domain or mail server.

## Files
- `index.html` — interface and API client
- `manifest.json` — installable web app metadata
- `sw.js` — caches the app shell for faster repeat visits
- `icon.svg` — app icon

## Deploy free with GitHub Pages (Android phone)
1. Sign in at https://github.com/ and create a new public repository, e.g. `quickinbox`.
2. Open the repository in your browser, choose **Add file → Create new file**.
3. Create each file in this folder with the exact filename and paste its contents.
4. Open **Settings → Pages**. Under build/deployment, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
5. Wait for GitHub Pages to publish. The URL is usually `https://YOUR-USERNAME.github.io/quickinbox/`.
6. Open the URL in Chrome on Android. Use Chrome menu `⋮` → **Install app** or **Add to Home screen**.

## Notes
- Mail.tm API availability, domains, delivery and message retention are controlled by Mail.tm. Some sites block disposable email addresses.
- Attribution to Mail.tm is included in the page. Respect the provider's terms: https://docs.mail.tm/
- The browser stores the inbox password and bearer token in localStorage on this device. Do not use a shared phone or any sensitive account. Clearing browser storage loses access to the saved inbox.
- The app displays message bodies as plain text to avoid executing HTML from untrusted emails.
- It needs internet access to create inboxes and fetch messages; offline caching only covers the app shell.
- This is a personal client using Mail.tm, not a custom-domain email service.
