# Responsible AI group — website

Source of <https://rai-uu.github.io/>, the website of the Responsible AI group at Utrecht University. It is a plain static site served by GitHub Pages: no build step.

## Updating content

Almost everything is in **`js/data.js`**:

| To… | Edit in `js/data.js` |
|---|---|
| add a news item | copy an entry in `news` (types: award, paper, people, event, talk, grant, role, defence, media) |
| add a member | copy an entry in `people`; add a square photo (~600 px) to `images/people/` |
| move someone to alumni | move their entry from `people` to `alumni` and fill in `now` |
| add a course | copy an entry in `courses` (`level` is `MSc`, `BSc` or `Interdisciplinary`) |
| add an MSc thesis | copy an entry in `theses` (put the code in a `rai-uu` repository) |
| add a publication | copy an entry in **`js/publications.js`** |

Text fields accept `*italic*` and `[link text](https://...)`. Pages update automatically; counts on the home page are computed.

## Files

- `index.html`, `research.html`, `team.html`, `news.html`, `publications.html`, `education.html`: page layouts.
- `js/site.js`: shared header and footer, and the code that turns `data.js` into HTML.
- `css/site.css`: all styling (UU yellow and black, light and dark mode).
- `projects.html`: redirect to `research.html` for old links.

## Preview locally

```bash
python3 -m http.server 8765
```

Then open <http://localhost:8765>.
