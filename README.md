# JAE Kid Quizzes

Personalised nightly maths quizzes for children. Built by JAE Enterprise.

Each quiz is a single self-contained web page — no login, no account, no app to
install. Progress saves on the child's own device, so it plays even with no
signal. If the backend is reachable it also backs progress up so a parent can
see how they're going.

## Live quizzes

| Theme | Year level | Link |
|---|---|---|
| Pole Position (F1) | 7–8 | `/viraj/` |
| World Tour (popstar) | 5 | `/world-tour/` |
| Demo | — | `/demo/` |

## Folder names are public — don't put a child's name in one

`/world-tour/` is named after the theme, not the child who plays it. Anyone can
read a URL, so the child's first name stays inside the page where only they see
it. `/viraj/` predates this rule.

## Adding another child

1. Copy an existing folder and rename it after the **theme**, lowercase, hyphens
2. In that folder's `index.html`, change `const KID = '...'` to the child's first
   name (lowercase) — this is the private key their progress saves under
3. Change the `<title>`, the `<h1>`, the localStorage key `<name>-state-v2`, the
   sound key `<name>-sound`, and every name in the word-problem `names` array
4. Run the generator stress test before it goes anywhere near a child
5. Commit and push — the link is live in about a minute

No Google setup, ever. One shared backend serves every child.
