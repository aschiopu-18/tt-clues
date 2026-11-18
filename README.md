# tt-clues: teammate page for the Split Clues challenge

The team phone shows QR codes that open this page with a clue in the link
(`index.html#v1|team|player|players|tokens`). Nothing is stored on a server.

## Publish on GitHub Pages (once)
1. On github.com (account aschiopu-18) create a new **public** repository named `tt-clues`.
2. Upload `index.html` from this folder (Add file > Upload files > Commit).
3. Settings > Pages > Source: "Deploy from a branch", Branch: `main`, folder `/ (root)` > Save.
4. After a minute the page is live at https://aschiopu-18.github.io/tt-clues/
   (that is ClueChallenge.DefaultBaseUrl in the app).

Using another address? Put it in `"clueBaseUrl"` at the top of the objectives JSON.

## Link format
`#v2|team|player|players|seed|tokens` (URL-encoded). The seed picks each player's emoji rebus
from `REBUS` in index.html; solving it unlocks the clue. Old `v1|team|player|players|tokens`
links (no rebus) still work. Tokens are joined with `.`, e.g. `S17`,
`P13=9`, `X2=4`. A clue about the building is `Q<digit>~<base64url sentence>`. The sentences in
`clueText()` must stay identical to `CluePuzzle.Clue.Text()` in the app.

## Updating the live page
Upload the new `index.html` to the `tt-clues` repository again (Add file > Upload files).
