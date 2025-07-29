# wanikani_sentences
WaniKani sentence practice browser-only tool

I quickly mocked up this “WaniKani Sentence Practice” browser-only tool. It…

* Uses your WaniKani API key to fetch vocab with reviews due in 1–7 days (probably should make this adjustable, I just wanted some limit)
* Shows one random context sentence per vocab word
* Lets you press Space to reveal English and continue, or 1 to mark “didn’t know”
* Skips sentences you’ve already seen today
* Randomizes the vocab order
* Randomizes the Japanese display font (would be great to be able to turn this off. Or say “don’t use this font anymore”.
* Tracks progress and review history in localStorage (although this progress tracking isn’t utilized in any way at this point, tbh I’m not sure I care. I just want to read sentences, so I’m just smashing the space bar).

No server or install needed — just open the file in a browser.
