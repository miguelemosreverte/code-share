# code-share

A tiny live code-sharing page for Scala and Haskell snippets.

**Open:** https://miguelemosreverte.github.io/code-share/

- Each snippet has its own link (`#id`). Open it and start typing; anyone with the link sees the changes live, syntax-highlighted.
- **New** starts an empty snippet, **Copy link** shares the current one.
- No login, no build step: one `index.html` with CodeMirror for highlighting and the Firebase Realtime Database REST API for sync (Server-Sent Events in, debounced `PUT` out).

Snippets are stored at `/code-share/snippets/<id>` and are public: anyone with the link can read and edit them. If two people type at the same moment, the last write wins.
