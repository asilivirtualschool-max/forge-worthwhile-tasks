# Tasks Worth Setting

The website and self-paced course for **Tasks Worth Setting** — a seven-module professional development course on designing for intellectual demand and access, safely, with AI in the room.

**Live:** https://asilivirtualschool-max.github.io/forge-worthwhile-tasks/

---

## What is in this repository

| File | What it is |
| --- | --- |
| `index.html` | The website. Course overview, the safeguarding argument, the seven modules, pricing calculator for live training, and the booking enquiry form. |
| `course.html` | The self-paced course itself. One self-contained file: seven modules, two gates, three portfolio pieces, a final assessment and a certificate. |
| `summary.pdf` | The 16-page course summary and compliance dossier, written for reviewers and school leaders. Clickable contents, PDF bookmarks, one page in Arabic. |
| `.nojekyll` | Stops GitHub Pages running the files through Jekyll. |

No build step, no dependencies, no framework. Open `index.html` in a browser and the site works.

## Delivery and pricing

| | |
| --- | --- |
| **Self-paced** | Priced on enquiry, per seat or as a school-wide licence. |
| **Virtual training** | **AED 200 per teacher, per one-hour session.** Four-hour minimum, so AED 800 per teacher at the floor. Includes the 90-minute Integration Clinic at day 30. |

The rate and the minimum live in one place — the `CONFIG` block at the top of the script in `index.html`:

```js
var RATE = 200;            // AED per teacher, per one-hour session
var HOURS_PER_SESSION = 1;
var MIN_SESSIONS = 4;      // the four-hour minimum
```

Change those three values and the calculator, the breakdown and the enquiry email all follow.

## Before you publish

**The booking address is set** to `asilivirtualschool@gmail.com`, in the same `CONFIG` block:

```js
var CONTACT_EMAIL = "asilivirtualschool@gmail.com";
```

Change that one line if enquiries should go somewhere else. It drives the mailto link, the "Or just write" box, and the copied enquiry text. Nothing else needs editing.

## How the site handles data

Nothing is collected. No account, no server, no analytics, no cookies, and no form posted anywhere. The booking form composes an enquiry and opens it in the visitor's own email client, with a copy-to-clipboard fallback. The course stores progress and portfolio text in the learner's own browser via `localStorage`, which never reaches the school or Forge.

This is deliberate rather than a limitation: the course's final module argues that the lowest-collection architecture is the right default, and the site is built the way the course says to build things. The one consequence worth naming is that the course certificate is self-declared and is **not verified training evidence** — see the dossier.

## Accessibility

Keyboard reachable throughout, WCAG 2.1 AA contrast in light and dark themes, reflows to 320px with no horizontal scrolling, animation disabled under `prefers-reduced-motion`, Arabic marked `lang="ar"` with `dir="rtl"`. Not yet tested with a screen reader by a user of one.

## Attribution

The course teaches the **Transforming Tasks** strategies and techniques, developed and published by the **South Australian Department for Education** within its Teaching for Effective Learning (TfEL) framework. Forge is not affiliated with, endorsed by, or acting on behalf of the Department. The framework is theirs; the examples, module structure, assessment design and AI application are ours.

> **Before any commercial use**, the licensing position for the underlying Transforming Tasks materials must be confirmed in writing with the South Australian Department for Education.

It also draws on the differentiated instruction model of **Carol Ann Tomlinson**; the *A.C.C.E.S.S. Differentiation Handbook* (Hockett, Tennessee Department of Education, 2018); the **SAMR** model of Ruben Puentedura, together with published criticism of its use as a hierarchy; and fluency and fluency plus (Westwell). Full references are in `summary.pdf` and in the course appendix.

Legal content is written from published sources and has **not yet been reviewed by a qualified UAE legal practitioner**. It is orientation, not legal advice.

## Accreditation

This course carries **no statutory accreditation** in the UAE, the wider Gulf, Kenya or Nigeria, and no licence credit in any jurisdiction. It is not approved by KHDA or any regulator.

## Licence

© Forge, part of Edu Forge. All rights reserved. Not licensed for redistribution, resale or re-teaching without a written agreement.

Robert Wanyoike · Forge · Dubai
