# WaniKani Sentences
WaniKani sentence practice browser-only tool.

This is a WaniKani Sentence Practice tool that works entirely in your browser. It:

* Uses your WaniKani API key to fetch WaniKani sentences with vocabulary based on your selected Study Mode.
* Groups items into manageable chunks based on your defined Batch Size.
* Shows one random context sentence per vocab word.
* Lets you press Space to reveal the English translation and continue, or 1 to mark “didn’t know”.
* Skips sentences you’ve already seen inside an active iteration cycle.
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

### Option 2: Hosting it on GitHub Pages (Recommended)
Since it's just pure static front-end code, you can easily host this project for free using GitHub Pages. 
1. Push this code to a repository on GitHub.
2. Go to the repository **Settings** -> **Pages**.
3. Set the source "Branch" to `main` and click Save.
4. GitHub will give you a live URL. Visit that URL on your phone to "Add to Home Screen". Any future `git push` will automatically update the app on your phone!

# Study Modes

In the settings (gear icon), you can choose your desired Study Mode:

**Review Mode**
You use "Start (min) day offset" and "End (max) day offset" to select what period of time in the future you want to be studying for. If you select 0 and 1, you will be studying vocab from today's set of WaniKani reviews. If you select 1 and 2, you will be reviewing vocab that WaniKani will be showing you tomorrow.

**Recent Lessons**
Pulls vocabulary from your most recent user-defined pool of lessons (configurable via "Recent Pool Size", default 30). This allows you to practice strictly newly learned items until you've cycled through all of them.

**Burned Items**
Shuffles vocabulary items that you have successfully "Burned" in WaniKani. Once you review a burned item, you will not see it again until you have completely cycled through your entire WaniKani burned collection!

---

## Batch Learning System
To keep study sessions manageable, the application limits the amount of vocabulary loaded at once based on your "Batch Size (n)" setting. Once you complete a batch, a button will appear (or you can just press **Space**) to instantly load the next batch of unseen vocabulary without reloading the page. Items reviewed are remembered by Study Mode so you never do duplicates in the same run!

---

### Local Text-To-Speech Note
"Local Text-to-Speech" relies on your browser or operating system's built-in Japanese speech synthesis voices. 
- Windows/macOS/iOS/Android generally have Japanese voices pre-installed.
- **Linux** often does not have Japanese voices installed by default. If the voice list is empty or fails to read Japanese, use the "Google Translate" audio mode, or install a Japanese TTS package for your distro (like `speech-dispatcher`).
