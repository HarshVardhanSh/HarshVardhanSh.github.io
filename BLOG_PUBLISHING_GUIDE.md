# Publishing a Research Note

The site reads every post from `blog/posts.js`. The homepage shows the newest three published notes, while `blog/index.html` shows the complete published archive.

## Folder structure

```text
harshvardhansh.github.io/
├── index.html
├── assets/
│   ├── harsh_profile.jpg
│   └── Harsh_Shrivastava_CV.pdf
└── blog/
    ├── index.html
    ├── posts.js
    └── posts/
        └── 2026-09-understanding-natural-direct-effects.pdf
```

## Publish from Overleaf

1. Finish and compile the note in Overleaf.
2. Download the final PDF.
3. Rename it with lowercase letters, numbers, and hyphens. A useful pattern is `YYYY-MM-short-title.pdf`.
4. Put the PDF in `blog/posts/`.
5. Open `blog/posts.js` and add a new object at the top of `window.BLOG_POSTS`.
6. Confirm that the `pdf` value matches the uploaded filename exactly.
7. Set `published` to `true` only after the PDF is present.
8. Commit and push the changed files to the GitHub Pages repository.

## Metadata template

```javascript
{
  "title": "Your Note Title",
  "date": "2026-10-05",
  "summary": "A two- or three-sentence abstract that tells readers what the note explains.",
  "tags": ["Causal Inference", "Causal Discovery"],
  "readingMinutes": 14,
  "pdf": "posts/2026-10-your-note-title.pdf",
  "published": true
}
```

Separate neighboring objects with a comma. Keep dates in `YYYY-MM-DD` format so sorting remains reliable.

## Draft behavior

Use `"published": false` while preparing an entry. Draft entries remain in `posts.js` but are hidden from both the homepage and the archive. The included example is hidden by default and can be edited into your first real post.
