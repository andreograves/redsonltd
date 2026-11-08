# Update the Red Son logo on andreograves.com

redsonltd.com now uses a new logo: boxy letters with three speed stripes across the
lower half of each row, and an eclipsing period. andreograves.com draws the Red Son logo
itself as inline SVG, so it still shows the old stencil version until these three
snippets are swapped in. The logo is drawn shapes, not a font, so there is nothing to
install or load.

Hand this file to the session or person editing the andreograves.com repo. `andreograves-logo-preview.png`, next to this file, shows all three rendered with that site's CSS.

## What to change

All three are in `index.html`. Replace each **whole** `<svg>…</svg>` element, from the
opening `<svg` to its closing `</svg>`. Leave the surrounding `<a>`, `<figure>` and `<h3>`
tags, and all CSS, exactly as they are.

| # | Where | Find the `<svg>` that is inside… |
|---|---|---|
| 1 | Link list (one-line wordmark) | `<a class="t-rs" href="https://redsonltd.com/" …>` |
| 2 | Red Son project card (stacked logo above the sun) | `<figure class="rs">`, the one with `class="rs-mark"` |
| 3 | Red Son project card caption (small wordmark) | `<div class="meta"><h3 class="t-rs" …>` |

No CSS changes are needed. The new SVGs use the classes already styled on that page:
`rs-word`, `rs-mark` and `son`, plus `currentColor` and `var(--rs-red)`. Red SON, the
red-on-hover effect, the drop shadow and the sizes all keep working.

Each snippet has its own mask id (`rs-word-nav`, `rs-mark-card`, `rs-word-card`). These
make the stripes, so keep them unique: don't paste the same snippet twice.

## 1. Link list wordmark

```html
<svg class="rs-word" viewBox="-4 -4 1158 110" aria-hidden="true"><defs><mask id="rs-word-nav" maskUnits="userSpaceOnUse" x="-4" y="-4" width="1158" height="110"><rect x="-4" y="-4" width="1158" height="110" fill="#fff"/><rect x="-4" y="65" width="1108" height="3" fill="#000"/><rect x="-4" y="73" width="1108" height="4" fill="#000"/><rect x="-4" y="83" width="1108" height="5" fill="#000"/></mask></defs><g mask="url(#rs-word-nav)"><path fill="none" stroke="currentColor" stroke-width="26" d="M13 100V13H75A12 12 0 0 1 87 25V46A12 12 0 0 1 75 58H13 M210 13H135A12 12 0 0 0 123 25V75A12 12 0 0 0 135 87H210M123 50H198 M233 100V13H295A12 12 0 0 1 307 25V75A12 12 0 0 1 295 87H220 M793 0V75A12 12 0 0 0 805 87H880 M890 13H990M940 26V100 M1013 100V13H1075A12 12 0 0 1 1087 25V75A12 12 0 0 1 1075 87H1000"/><g fill="currentColor"><path d="M48 58H78L100 96V100H70Z"/></g><g class="son"><path fill="none" stroke-width="26" d="M490 13H415A12 12 0 0 0 403 25V38A12 12 0 0 0 415 50H465A12 12 0 0 1 477 62V75A12 12 0 0 1 465 87H390 M525 13H575A12 12 0 0 1 587 25V75A12 12 0 0 1 575 87H525A12 12 0 0 1 513 75V25A12 12 0 0 1 525 13Z"/><path d="M610 0H640L684 61V0H710V100H680L636 39V100H610Z"/></g></g><circle cx="1123" cy="86" r="16" fill="currentColor"/><circle class="son" cx="1134" cy="75" r="16"/></svg>
```

## 2. Project card stacked logo

```html
<svg xmlns="http://www.w3.org/2000/svg" viewBox="-4 -4 382 330" class="rs-mark" aria-hidden="true"><defs><mask id="rs-mark-card" maskUnits="userSpaceOnUse" x="-4" y="-4" width="382" height="330"><rect x="-4" y="-4" width="382" height="330" fill="#fff"/><rect x="-4" y="65" width="330" height="3" fill="#000"/><rect x="-4" y="73" width="330" height="4" fill="#000"/><rect x="-4" y="83" width="330" height="5" fill="#000"/><rect x="-4" y="175" width="330" height="3" fill="#000"/><rect x="-4" y="183" width="330" height="4" fill="#000"/><rect x="-4" y="193" width="330" height="5" fill="#000"/><rect x="-4" y="285" width="330" height="3" fill="#000"/><rect x="-4" y="293" width="330" height="4" fill="#000"/><rect x="-4" y="303" width="330" height="5" fill="#000"/></mask></defs><g mask="url(#rs-mark-card)"><g fill="none" stroke="currentColor" stroke-width="26"><path d="M13 100V13H75A12 12 0 0 1 87 25V46A12 12 0 0 1 75 58H13 M210 13H135A12 12 0 0 0 123 25V75A12 12 0 0 0 135 87H210M123 50H198 M233 100V13H295A12 12 0 0 1 307 25V75A12 12 0 0 1 295 87H220"/><path transform="translate(0 220)" d="M13 0V75A12 12 0 0 0 25 87H100 M110 13H210M160 26V100 M233 100V13H295A12 12 0 0 1 307 25V75A12 12 0 0 1 295 87H220"/></g><g fill="currentColor"><path d="M48 58H78L100 96V100H70Z"/></g><g transform="translate(0 110)"><path fill="none" stroke="var(--rs-red)" stroke-width="26" d="M100 13H25A12 12 0 0 0 13 25V38A12 12 0 0 0 25 50H75A12 12 0 0 1 87 62V75A12 12 0 0 1 75 87H0 M135 13H185A12 12 0 0 1 197 25V75A12 12 0 0 1 185 87H135A12 12 0 0 1 123 75V25A12 12 0 0 1 135 13Z"/><g fill="var(--rs-red)"><path d="M220 0H250L294 61V0H320V100H290L246 39V100H220Z"/></g></g></g><circle cx="343" cy="306" r="16" fill="currentColor"/><circle cx="354" cy="295" r="16" fill="var(--rs-red)"/></svg>
```

## 3. Project card caption wordmark

```html
<svg class="rs-word" viewBox="-4 -4 1158 110" aria-hidden="true"><defs><mask id="rs-word-card" maskUnits="userSpaceOnUse" x="-4" y="-4" width="1158" height="110"><rect x="-4" y="-4" width="1158" height="110" fill="#fff"/><rect x="-4" y="65" width="1108" height="3" fill="#000"/><rect x="-4" y="73" width="1108" height="4" fill="#000"/><rect x="-4" y="83" width="1108" height="5" fill="#000"/></mask></defs><g mask="url(#rs-word-card)"><path fill="none" stroke="currentColor" stroke-width="26" d="M13 100V13H75A12 12 0 0 1 87 25V46A12 12 0 0 1 75 58H13 M210 13H135A12 12 0 0 0 123 25V75A12 12 0 0 0 135 87H210M123 50H198 M233 100V13H295A12 12 0 0 1 307 25V75A12 12 0 0 1 295 87H220 M793 0V75A12 12 0 0 0 805 87H880 M890 13H990M940 26V100 M1013 100V13H1075A12 12 0 0 1 1087 25V75A12 12 0 0 1 1075 87H1000"/><g fill="currentColor"><path d="M48 58H78L100 96V100H70Z"/></g><g class="son"><path fill="none" stroke-width="26" d="M490 13H415A12 12 0 0 0 403 25V38A12 12 0 0 0 415 50H465A12 12 0 0 1 477 62V75A12 12 0 0 1 465 87H390 M525 13H575A12 12 0 0 1 587 25V75A12 12 0 0 1 575 87H525A12 12 0 0 1 513 75V25A12 12 0 0 1 525 13Z"/><path d="M610 0H640L684 61V0H710V100H680L636 39V100H610Z"/></g></g><circle cx="1123" cy="86" r="16" fill="currentColor"/><circle class="son" cx="1134" cy="75" r="16"/></svg>
```

## Check it

Open andreograves.com and confirm:

- The link-list entry and the card caption read **RED SON LTD.** on one line in the
  striped letters: SON in red, the rest in the page text colour, and a red-over-dark dot
  at the end.
- Hovering the link-list entry turns the whole wordmark red.
- The Red Son card shows the stacked three-row logo in cream and red above the red half sun.

## Link previews (iMessage, Slack, Facebook)

When someone shares `https://redsonltd.com/`, the preview card uses
`https://redsonltd.com/img/share.jpg`, which already shows the new logo. Apps cache
previews, so an old card can linger. To refresh it:

- Facebook / Instagram: paste the URL into the Sharing Debugger
  (developers.facebook.com/tools/debug) and click **Scrape Again**.
- LinkedIn: paste it into the Post Inspector (linkedin.com/post-inspector).
- Slack / iMessage: these refresh on their own after a while. Sharing
  `https://redsonltd.com/?v=2` forces a fresh card immediately.

