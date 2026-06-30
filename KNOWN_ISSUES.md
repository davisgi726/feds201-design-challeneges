# Known Issues — FEDS 201 Design Challenges

Running log of bugs, quirks, and things to investigate. Add new entries at the top. Mark resolved items with ✅ and the date fixed rather than deleting them — useful history.

---

## Open Issues

### PPTX rendering looks off when opened in Chrome's built-in viewer (Chromebook)
**Status:** Open — investigating
**Reported:** Testing of Challenge 01, first student test round
**Symptom:** When a student downloads the generated .pptx on a Chromebook and opens it with Chrome's built-in viewer (or the Google Drive quick-view), formatting looks degraded — spacing, fonts, or layout don't match what PptxGenJS intended. Students can still submit the file successfully.
**Likely cause:** Chrome's built-in Office file viewer (and Google's quick-view preview) uses a simplified rendering engine that doesn't fully support all PowerPoint formatting features PptxGenJS generates (custom fonts, certain shape/text positioning, gradients). This is a known limitation of lightweight web-based PPTX viewers generally, not necessarily a bug in our generation code.
**Workaround for now:** Students can still submit the file as-is; the underlying file data is intact. To verify, open the same file in actual PowerPoint or Google Slides (File → Open with → Google Slides) — formatting should display correctly there.
**To investigate:**
- [ ] Confirm whether the file renders correctly when uploaded to Google Slides (would confirm it's a Chrome quick-view limitation, not a generation bug)
- [ ] Check if specific fonts (Cambria, Calibri) are the issue — these may not be installed/substituted properly in Chrome's viewer
- [ ] Consider simplifying font usage to web-safe fonts if this persists
- [ ] Test on a non-Chromebook (Windows/Mac with real PowerPoint) to compare

---

## Resolved Issues

*(none yet — first entries will go here as issues are fixed)*

---

## How to use this file

When you or a student finds something broken:
1. Add a new entry under **Open Issues** with today's date
2. Describe the symptom (what you saw) separately from any suspected cause
3. If there's a workaround, note it so it doesn't block other work
4. When fixed, move the entry to **Resolved Issues** with the fix date and a one-line summary of what changed
