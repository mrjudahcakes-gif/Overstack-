OVERSTACK - PHONE APP

=== EASIEST: GET THE APK WITHOUT INSTALLING ANYTHING (free, about 15 minutes) ===
GitHub can build the APK for you in the cloud.
1. Make a free account at https://github.com
2. Click "+" (top right) > New repository. Name it "overstack", leave the rest, click Create repository.
3. Open the repository on github.com (on a phone use Chrome with "Desktop site" turned on). Click "Add file" > "Upload files"
   and pick these files: index.html, package.json, capacitor.config.json, icon-512.png, github-build-apk.yml.
   No folders needed. Click "Commit changes".
4. Click "Add file" > "Create new file". For the name type exactly:   .github/workflows/build-apk.yml
   Open github-build-apk.yml from this folder, copy everything in it, paste it into the big box, click "Commit changes".
5. Click the "Actions" tab. A "Build APK" run starts (5-10 minutes). When it shows a green check, click it,
   scroll to "Artifacts" and download "overstack-apk". Unzip it: inside is app-debug.apk.
6. Send app-debug.apk to friends through WhatsApp, Discord, Telegram, Quick Share or the Google Drive app.
   They tap it and allow "Install unknown apps" when Android asks.
If the run shows a red X, open it and send the error text to whoever is helping you.
Updating later: upload the new index.html to the repository (same place) and a new APK builds automatically.

OVERSTACK - PHONE APP (no web browser needed to install or play)

=== ANDROID (APK file) ===
You need a computer with:
- Node.js (LTS): https://nodejs.org
- Android Studio: https://developer.android.com/studio

1. Open a terminal in this folder and run:
     npm install
     npx cap add android
     npx cap sync
     npx cap open android
2. Android Studio opens. Wait until syncing finishes (bottom status bar).
3. Optional app icon: right-click "app" > New > Image Asset > pick icon-512.png from this folder.
4. Menu: Build > Build App Bundle(s) / APK(s) > Build APK(s). Click "locate" when done.
   The file is app-debug.apk.
5. Send the APK to friends WITHOUT a browser: WhatsApp, Discord, Telegram, Quick Share,
   or the Google Drive app. They tap the file, allow "Install unknown apps" for that app
   when Android asks, and it installs like any app.
   Note: if a phone has parental controls that block installing apps from outside the
   Play Store, it can only get the game through Google Play (needs a Play Console account).

=== IPHONE (TestFlight) ===
iPhones can't install APK files. You need a Mac with Xcode and the Apple Developer Program
(paid yearly membership).
1. In this folder on the Mac:  npm install, then  npx cap add ios,  npx cap sync,  npx cap open ios
2. In Xcode: select the "App" target > Signing & Capabilities > choose your Team.
3. Product > Archive, then Distribute App > App Store Connect > Upload.
4. In App Store Connect (appstoreconnect.apple.com) > your app > TestFlight, add your friends
   as testers using their Apple ID email.
5. Friends install the free "TestFlight" app from the App Store, then open TestFlight and
   tap "Redeem" with the code from their invite email. No browser needed.

=== Updating the game ===
Replace www/index.html with the new version, run  npx cap sync,  and build again.
Friends install the new APK over the old one (their save is kept), or get the TestFlight update.
