# Simmer app (Android + iOS wrapper)

## Fastest way, no build (works on both phones)
1. Upload the `www` folder to any HTTPS host (Netlify Drop, Vercel, GitHub Pages, Cloudflare Pages).
2. Open the link on the phone.
   - Android Chrome: menu > Install app
   - iPhone Safari: Share > Add to Home Screen
   It then opens full screen with the Simmer icon, like a real app.

## Android APK (free, built in the cloud)
1. Create a GitHub repo and upload everything in this folder.
2. Go to Actions > "Build Android APK" > Run workflow.
3. When it finishes, download the artifact "Simmer-debug-apk", unzip, install app-debug.apk
   (allow "install unknown apps" on the phone).

## iOS
iOS needs a Mac with Xcode and an Apple Developer account ($99/yr) to install outside the browser.
On a Mac: `npm install && npx cap add ios && npx cap sync ios && npx cap open ios`, then press Run.
For TestFlight without owning a Mac, use a cloud builder such as Codemagic or Expo EAS.
