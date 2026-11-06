# Luna's Reading Adventure

Voice-first reading app for kids 4 to 6 (90-day program). Luna, a friendly moon, reads aloud, listens, and cheers your child on through short daily sessions.

**Live:** https://emresenturer.github.io/lunas-reading-adventure/

## What it does

- **90 real days in 6 phases** (15 days each): letter sounds, blending CVC words, sight words, short phrases, simple sentences, tiny stories. Every day is generated from embedded word lists and stories, so all 90 days are distinct.
- **3 to 5 minute sessions** of 6 to 8 activities: Luna says a sound, word or sentence, and the child picks the matching picture or word, or says it back.
- **Never punishing.** A wrong tap dims that card and Luna gently repeats the prompt. Every finished activity earns a star.
- **Voice in, voice out.** Luna speaks with the browser's built-in speech synthesis. Where speech recognition exists (Chrome, Edge, Safari on macOS), the child taps the mic and says the word. Matching is forgiving: punctuation, digits ("2" for "two"), soundalikes ("to" for "two") and close matches all count, and after two misses Luna praises the effort and moves on. Where recognition is missing (Firefox, iOS), the child says it out loud and taps a big "I said it!" button.
- **Progress map, streak and stars** saved in localStorage.
- **Grown-ups corner** behind a 3 second press and hold: progress by phase, talking speed, microphone on or off, open all days, tips, progress export (.md), and a two-step reset.
- Huge tap targets and the Andika font (designed for beginning readers). Works at 390px portrait, tablets and desktop. Light and dark themes.

## Run locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000/.

## Privacy

No account, no server, no analytics, no AI model. Progress lives only in this browser's localStorage. Some browsers (for example Chrome) send speech recognition audio to the browser maker's online service; parents can turn the microphone off in the grown-ups corner and use tap-to-answer instead.

## Stack

One `index.html`: plain HTML, CSS and JavaScript, inline SVG for Luna, Web Speech API (speechSynthesis and SpeechRecognition / webkitSpeechRecognition), localStorage. No build step, no dependencies besides the optional Google Fonts stylesheet.

## License

MIT, see [LICENSE](LICENSE).
