# Code Reps

A tiny website for building coding skills with small daily practice. Write a JavaScript function in the browser, run the tests, and track your progress through a 30-day plan.

Everything runs client-side. There is no build step and no backend. Progress is saved in your browser's `localStorage`.

## Features

- Five practice challenges with in-browser test runner
- Hints, code reset, and Ctrl/Cmd + Enter to run
- 40 lessons (20 JavaScript, 20 HTML + CSS) that check your code and award credits
- Credits (5 per lesson, 10 per challenge) that buy back missed days for 10 each
- Calendar showing practiced, missed, and bought-back days
- Mouse-following grid animation in the background
- Playground: run JavaScript, Python (loaded from a CDN on first use, needs internet), or HTML + CSS + JS on the page, with a console and live preview
- Day streak and solved counter
- 30-day plan checklist
- Light and dark mode

## Run locally

Open `index.html` in your browser.

## Deploy with GitHub Pages

1. Create a new repository on GitHub (for example `code-reps`).
2. Upload `index.html` and `README.md` to the repository root.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
5. After a minute, your site is live at `https://<your-username>.github.io/code-reps/`.

## Add your own challenge

In `index.html`, add an object to the `CH` array:

```js
{
  id: 'unique-id',
  fn: 'functionName',
  title: 'Challenge title',
  lvl: 'Easy',
  prompt: 'What the function should do.',
  starter: 'function functionName(x) {\n  \n}',
  hint: 'A nudge in the right direction.',
  tests: [{ a: [input], e: expectedOutput }]
}
```

`a` is the list of arguments passed to the function and `e` is the expected return value.

## Ideas to grow it

- More challenges, grouped by topic
- A Python mode using Pyodide
- Share a solved-challenge badge on your profile README
- Add a GitHub Actions workflow that lints the file on every push

## License

MIT
