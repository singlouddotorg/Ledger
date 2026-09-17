# Simple Totals

**Version 0.1** — new, not yet in wide use.

Load any number of finished singings — Simple Minutes exports, Simple Compile source
files, or Master CSVs from the full Minutes app — and get one combined record plus real
totals across all of them: what's been sung most, from which books, and by which leaders.
Built for anyone keeping a master record across a regular singing's many occurrences,
without hand-merging CSVs in a spreadsheet.

One HTML file, plus the same shared tunebook library and utilities the rest of the Suite
uses. Nothing to install, no server, no build step.

## Part of the Sing Loud Suite

| App | What it does | Status |
|---|---|---|
| [**Minutes**](https://github.com/singlouddotorg/minutes) | Log a singing as it happens, then turn that log into publishable minutes — with full editing. | Beta |
| [**Tunebooks**](https://github.com/singlouddotorg/tunebooks) | Curate the shared tunebook data — editions, page indexes, Level 3 scholarly files. | Beta |
| [**Simple Minutes**](https://github.com/singlouddotorg/Simple-Minutes) | A phone-sized logger: page numbers only, no names. Its files import straight into Minutes, Simple Compile, and Simple Totals. | 1.0 release |
| [**Simple Compile**](https://github.com/singlouddotorg/Simple-Compile) | A one-page, no-editing version of Minutes: open a CSV, get readable minutes back. | 1.0 release |
| **Simple Totals** | This app. | New (0.1) |
| [**Tunebook Registry**](https://github.com/singlouddotorg/tunebook-registry) | The published tunebook data the others read. | 1.0 release |

## What It Is For

Someone running a regular singing — a monthly local sing, an annual convention — often
wants, after a year or a decade of occurrences, a real answer to "what have we actually
sung the most," "how many times has this song come up," or "who's led the most songs at
our singing." Every individual singing already has this in miniature (Minutes shows a
tally for one singing's own Capture log), but nothing before this combined it across many
singings without manually pasting rows together in a spreadsheet — a real hassle once
there are dozens of files, and an easy way to double-count or miss one by hand.

Simple Totals does exactly that one thing: load every finished singing you have, and it
adds them all up.

## Using It

1. Open `index.html` and choose or drop in as many CSV files as you like, all at once or
   over several visits — Simple Minutes exports, Simple Compile source files, and Master
   CSVs from Minutes can all be mixed together.
2. Check the loaded-singings list for anything flagged as a likely duplicate (the same
   singing loaded twice, most often by accident) — a flagged file stays visible but is left
   out of the totals until you tap **Include anyway**.
3. Read **Song frequency**, **By book**, and **By leader** — each totals across every
   singing currently loaded.
4. **Download combined CSV** for one file with every song from every singing, or
   **Download totals CSV** for the three tables as their own file, ready for a spreadsheet.
5. **Reset all** clears every loaded singing at once, with a confirmation first, so a new
   batch of files can be totaled from a clean slate.

## Nothing Is Edited, Nothing Is Uploaded

Simple Totals has no editing surface at all — it only reads what's already in each file and
adds it up. Every file is read once, in the browser; nothing is sent anywhere, and nothing
is written to browser storage between visits. If a name or page genuinely needs correcting
before it's totaled, do that first in the full [Minutes](https://github.com/singlouddotorg/minutes) app, then load the
corrected file here.

## Where the Songbook Data Comes From

`tunebook-library.js` ships bundled right beside `index.html`, exactly like every other app
in this suite — read strictly as data, never executed as code. It's used only to turn a
stored edition code back into a real book name for the By Book totals; the CSV itself
stores the code, not the name.
