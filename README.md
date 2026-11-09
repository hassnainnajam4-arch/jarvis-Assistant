# JARVIS Android PWA

A starter personal voice assistant for Android Chrome. It supports typed and speech input, multilingual prompting (Urdu, Roman Urdu, Sindhi, English), spoken answers, and a female-voice preference using voices installed on the phone.

## Run it
1. Extract this ZIP.
2. Host the folder on an HTTPS static host (for example GitHub Pages or Netlify). Microphone access generally requires HTTPS.
3. Open the HTTPS link in Chrome on Android.
4. Open Settings in JARVIS, paste your OpenAI API key, choose a speech-recognition language, and save.
5. Chrome menu (⋮) → **Add to Home screen** / **Install app**.

## Important limitations
- This is a PWA starter, not a signed APK. An APK requires packaging/signing with Android tooling.
- Browser speech recognition availability and language support vary by Android device/browser. Urdu and English are commonly available; Sindhi recognition may not be supported on every device. Choose the closest available language or type if recognition fails.
- Female text-to-speech depends on voices installed on the phone. The app prefers a female-sounding voice when the device exposes one, but cannot guarantee a female Urdu/Sindhi voice.
- AI replies need internet and an OpenAI API key. API usage may incur charges.
- The API key is stored in this browser's local storage. This is convenient for a personal prototype but not secure against someone with access to the device/browser. Do not publish the app with your key embedded.
- The model is instructed to mirror the language and script of the latest message. Mixed-language detection is approximate and depends on the model.

## Files
- `index.html` — app interface and logic
- `manifest.json` — install metadata
- `sw.js` — offline shell cache
