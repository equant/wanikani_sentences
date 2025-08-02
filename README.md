# wanikani_sentences
WaniKani sentence practice browser-only tool.

I quickly mocked up this “WaniKani Sentence Practice” browser-only tool. It…

* Uses your WaniKani API key to fetch vocab with reviews upcoming reviews (in a user-definable time period).
* Shows one random context sentence per vocab word.
* Lets you press Space to reveal the English translation and continue, or 1 to mark “didn’t know”.
* Skips sentences you’ve already seen today.
* Randomizes the vocab order.
* Randomizes the Japanese display font (you can change what fonts, and the frequency of their use in the html source).
* Tracks progress and review history in localStorage (progress tracking isn’t utilized in any way at this point).
* This is not an SRS tool, it's just a reading WaniKani sentences review tool.

Just open the HTML file in a browser...

# How to Use/Install?

1. Download the index.html file from this repository.
2. Get your wanikani api from the wanikani site Account->Settings->Api Tokens (you will need to generate one if you haven't before)
3. Open the `index.html` file you downloaded with your favorite browser and paste the API key into the popup that asks for it.  Or, if for some reason you don't see a popup asking for the API key, you can click the gear icon and enter the key in the settings.

# What does the Start (min) End (max) day offset stuff mean?

In the settings, you use "Start (min) day offset" and "End (max) day offset" to select what period of time in the future you want to be studying for.  If you select 0 and 1, you will be studying vocab from today's set of WaniKani reviews.  If you select 1 and 2, you will be reviewing vocab that WaniKani will be showing you tomorrow.  If you select 7 and 14 you will be reviewing vocabulary that you won't be tested on (by WaniKani) until a week from now.  Etc.  Hope that makes sense.
