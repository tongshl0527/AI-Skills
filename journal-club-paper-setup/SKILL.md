---
name: Journal club paper setup
description: >-
  Use when the user has agreed to add a research paper to their journal club:
  saves the full PDF and a five-step-thinking study note as a Google Doc in a
  new per-paper subfolder of their Drive journal club folder.
---
# Journal club paper setup

Run only after the user said yes to this specific paper. Never share files with anyone.

## Inputs
- The paper's article URL (and DOI if known).
- The user's journal club Drive folder (from memory) and their naming convention for subfolders and study notes (from memory).

## Steps
1. **Read the paper metadata** from the article page: exact title, first author surname, journal, publication date, open access or not.
2. **Get the full PDF.**
   - Open access: download the publisher PDF with curl (follow redirects) to /workspace/journal-club/. Check it with `pdfinfo` (page count > 3, not an HTML error page).
   - Paywalled: use the box browser's signed-in institutional library session (see memory) via a browser task to download the PDF to /workspace/journal-club/. If no session works, stop and tell the user; never use unofficial sources.
   - Include the extended data/supplementary PDF only if it is part of the same publisher file.
3. **Read the full text** (pdftotext) so the study note rests on what the paper actually says, including figure legends, Methods and the peer review file if published.
4. **Create the subfolder** inside the journal club folder, named `FirstAuthor Journal Year - few words` (3–6 words about the paper). Check first that it doesn't already exist.
5. **Upload the PDF** into that subfolder, named `FirstAuthor_Journal_Year_short_topic.pdf`.
6. **Write the study note** in markdown, then create it as a formatted Google Doc in the same subfolder named `Study note - five-step thinking (FirstAuthor Journal Year)`. Structure:
   - Header: full citation with link; one line saying each step lists what to ask, where to look and the trap to avoid.
   - Five sections: 1. The question, and why now; 2. The key move; 3. The weakest load-bearing result; 4. The next experiment; 5. Why a top journal.
   - Under each: **Ask** (the generic questions), **Look** (where in this paper to look), **Trap** (common student mistake), **Paper example** (2–3 sentences specific to this paper, with real numbers/controls from the text).
   - Plain language, short. Never invent results, numbers or reviewer comments; only use what is in the paper or its review file.
7. **Verify**: list the subfolder contents and confirm both files are there; open the Doc to check formatting.
8. **Report** to the user in two lines with links to the subfolder, PDF and study note.
