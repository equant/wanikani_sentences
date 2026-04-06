# WaniKani Sentences
WaniKani sentence practice browser-only tool.

This is a WaniKani Sentence Practice tool that works entirely in your browser. It:

* Uses your WaniKani API key to fetch WaniKani sentences with vocabulary based on your selected Study Mode.
* Shows one random context sentence per vocab word.
* Lets you press Space to reveal the English translation and continue, or 1 to mark “didn’t know”.
* Skips sentences you’ve already seen today.
* Randomizes the vocab order.
* Randomizes the Japanese display font to improve reading flexibility.
* Tracks progress and review history in localStorage.

This is not an SRS tool, it's just a reading WaniKani sentences review tool.

## Progressive Web App (PWA) Support
This application is designed as a PWA, meaning it comes with a Service Worker (`sw.js`) and a App Manifest (`manifest.json`). This allows you to "Add to Homescreen" on your phone and use it like a native offline app.

To use all features, the app must be served over `http://localhost` or `https://` (meaning you usually can't just double-click `index.html` on your phone anymore).

# How to Use/Install?

### Option 1: Quick Testing Locally
To run this on your laptop, and to access it on your phone over Wi-Fi:
1. Open a terminal in this project folder.
2. Run a local web server: `python3 -m http.server 8000`
3. On your laptop, open a browser and navigate to `http://localhost:8000`.
4. On your phone, make sure you are on the same Wi-Fi network as your laptop. Find your laptop's local IP address (e.g. `192.168.1.5`). Open Safari or Chrome on your phone and go to `http://192.168.1.5:8000`. 
5. To install it on your phone: Tap "Share" (iOS) or the three-dot menu (Android) and choose "Add to Home Screen".

### Option 2: Hosting it Online
Since it's just pure HTML/JS, you can upload these 4 files (`index.html`, `sw.js`, `manifest.json`, `icon.svg`) to any free static host (like GitHub Pages, Netlify, or Vercel) and access the URL on your phone anytime, anywhere.

# Study Modes

In the settings (gear icon), you can choose your desired Study Mode:

**Review Mode**
You use "Start (min) day offset" and "End (max) day offset" to select what period of time in the future you want to be studying for. If you select 0 and 1, you will be studying vocab from today's set of WaniKani reviews. If you select 1 and 2, you will be reviewing vocab that WaniKani will be showing you tomorrow.

**Recent Lessons**
Pulls vocabulary from the last ~100 lessons you completed, ordered by when you first learned them.

**Burned Items**
Shuffles vocabulary items that you have successfully "Burned" in WaniKani.

---

### Local Text-To-Speech Note
"Local Text-to-Speech" relies on your browser or operating system's built-in Japanese speech synthesis voices. 
- Windows/macOS/iOS/Android generally have Japanese voices pre-installed.
- **Linux** often does not have Japanese voices installed by default. If the voice list is empty or fails to read Japanese, use the "Google Translate" audio mode, or install a Japanese TTS package for your distro (like `speech-dispatcher`).
