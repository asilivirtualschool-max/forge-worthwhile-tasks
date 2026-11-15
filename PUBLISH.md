# Publishing this site to GitHub Pages

Target: a public repo `forge-worthwhile-tasks` under `asilivirtualschool-max`,
live at **https://asilivirtualschool-max.github.io/forge-worthwhile-tasks/**

---

## Settings, if you need to change them

Everything configurable sits in one `CONFIG` block near the top of the `<script>` at the bottom of `index.html`:

```js
var CONTACT_EMAIL = "asilivirtualschool@gmail.com";
```

That is already set and drives the booking form, the mailto link and the copied enquiry text.

The rate sits just below it:

```js
var RATE = 200;            // AED per teacher, per one-hour session
var HOURS_PER_SESSION = 1;
var MIN_SESSIONS = 4;      // the four-hour minimum
```

---

## Route A — through the website, no git needed (about 3 minutes)

1. Go to **https://github.com/new**
2. Owner `asilivirtualschool-max`, repository name `forge-worthwhile-tasks`, **Public**.
   Leave "Add a README file" **unticked** — this folder already has one.
3. Create repository.
4. On the empty repo page, click **uploading an existing file**.
5. Drag in these five files from this folder:
   - `index.html`
   - `course.html`
   - `summary.pdf`
   - `README.md`
   - `.nojekyll`

   Drag the *files*, not the folder. Do not upload `PUBLISH.md` — it is only for you.
6. Commit message: `Publish Tasks Worth Setting` → **Commit changes**.
7. **Settings → Pages.** Source = **Deploy from a branch**, Branch = **main**, folder = **/ (root)**. Save.
8. Wait about a minute, then open
   https://asilivirtualschool-max.github.io/forge-worthwhile-tasks/

If Windows hides dotfiles and you cannot see `.nojekyll`, you can skip it — it only matters for sites with folders starting with an underscore, and this one has none.

---

## Route B — git, from a terminal in this folder

Create the empty repo on GitHub first (steps 1–3 above), then:

```bash
cd "forge-worthwhile-tasks"
git init -b main
git add index.html course.html summary.pdf README.md .nojekyll
git commit -m "Publish Tasks Worth Setting"
git remote add origin https://github.com/asilivirtualschool-max/forge-worthwhile-tasks.git
git push -u origin main
```

Then do step 7 above to switch Pages on.

To publish an update later:

```bash
git add -A
git commit -m "Update course"
git push
```

---

## Check these after it goes live

- The booking form opens an email addressed to `asilivirtualschool@gmail.com`.
- The pricing calculator reads **AED 200 / teacher / hour**, four-hour minimum, and the floor shows AED 800 per teacher.
- **Open the course** goes to `course.html` and the course footer links back to the site.
- **Summary for leaders** downloads `summary.pdf`.
- The page loads its fonts. If your network blocks Google Fonts the site still works — it falls back to Georgia and your system sans, and nothing breaks.

---

## Before you make it public

Two things carried over from the review, both still open:

1. **The Transforming Tasks licensing position** needs confirming in writing with the South Australian Department for Education before any commercial use. A public page selling training built on their framework is commercial use.
2. **The legal content has not been reviewed by a qualified UAE practitioner.** The site and the dossier both say so plainly, which is the right position until it has been. The new "What is established in law" section states the instruments and what each covers; it also states, in the same section, that naming KHDA is not a claim of approval.

A private repo now and a public one later is a legitimate choice. The site works identically either way.
