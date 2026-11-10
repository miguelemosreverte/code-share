# code-share

A tiny live code-sharing page for Scala and Haskell snippets.

**Open:** https://miguelemosreverte.github.io/code-share/

- Opening the page starts a snippet with its own link (`#id`); anyone with the link sees the code live, syntax-highlighted.
- A shared link shows only the code. **New** and **Copy link** appear only in the browser that created the snippet.
- Scala by default; add `?lang=haskell` to the link for Haskell (e.g. `.../code-share/?lang=haskell#abc123`).
- The coloured balls switch theme: Scastie (Solarized Dark), IntelliJ Darcula, IntelliJ Light. The choice is remembered per browser.
- The font grows to the largest size (11–28 px) at which the longest line still fits the screen, so short snippets read big on a phone.
- No login, no build step: one `index.html` with CodeMirror for highlighting and the Firebase Realtime Database REST API for sync (Server-Sent Events in, debounced `PUT` out).

Snippets are stored at `/code-share/snippets/<id>` and are public: anyone with the link can read and edit them. If two people type at the same moment, the last write wins.
