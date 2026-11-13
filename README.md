# File to Markdown (file2md)

Convert common office and text files to Markdown right in your browser. Batch-friendly, no install, and your files never leave your device.

**Live demo:** https://shainyhsu.github.io/file2md/

## Features

- Runs entirely client-side: nothing is uploaded to a server
- Batch conversion: drop or select several files at once
- Per file: preview, copy to clipboard, download `.md`, or remove
- Download all results as one ZIP, or clear everything
- Scanned PDFs without a text layer fall back to OCR (Traditional Chinese + English)
- Traditional Chinese / English interface (globe icon, top-right; Chinese by default)
- Light / dark theme toggle (top-right, dark by default; your choice is remembered)
- Two-column layout on wide screens (upload on the left, results on the right)
- Mobile-friendly downloads (UTF-8 `.md` files that open correctly on Android and iOS)

## Supported formats

| Type | Formats |
|------|---------|
| Documents | PDF, DOCX, PPTX |
| Spreadsheets | XLSX, XLS, CSV, TSV |
| Text | HTML/HTM, TXT, MD, JSON, XML |

- **PDF:** extracts the text layer when present; otherwise OCR with Tesseract.js (Traditional Chinese + English), with page-by-page progress
- **DOCX:** converted via mammoth and Turndown
- **PPTX:** text from each slide, under a `## Slide N` heading
- **XLSX / XLS:** each sheet becomes a Markdown table under its sheet name
- **CSV / TSV:** converted to a Markdown table
- **HTML:** converted with Turndown
- **JSON / XML:** wrapped in a code block (JSON is pretty-printed)

## How to use

1. Open the site
2. Drop or select one or more files
3. Preview, copy, or download each `.md`; use "Download all as ZIP" for a batch

## Tech

- mammoth, SheetJS, PDF.js, JSZip, Turndown, Tesseract.js (loaded from jsDelivr)
- Single `index.html`, no build step, hosted on GitHub Pages
- Search metadata: description, canonical URL, Open Graph and JSON-LD (WebApplication)
- Inspired by Microsoft MarkItDown, implemented entirely client-side

## Notes

OCR quality on scanned PDFs depends on image clarity and fonts. The first OCR run downloads language data, so it is slower. Proofread important documents.

## License

Copyright (c) 2026 Shainy Hsu. All rights reserved. See [LICENSE](LICENSE).

## Version history

Newest first. Times are Taiwan time (UTC+8). Also kept in [CHANGELOG.md](CHANGELOG.md).

- V16 | 2026-11-13 09:20 | Added a tab icon and an "All tools" link in the footer; the converter libraries load without holding up the page, and the file box has a label for screen readers.
- V15 | 2026-11-11 11:50 | Renamed to “檔案轉 Markdown / File to Markdown” (the forest-green look stays); page title, heading, search entries and link-preview image updated
- V14 | 2026-11-11 10:07 | New license terms: free to use in a browser for personal, work, school or club use, and the results you make are yours to share; copying, paid services built on it, and AI training need written permission. A License link sits at the bottom of the page
- V13 | 2026-11-10 00:18 | Added a link-preview image (1200×630) so shared links show a picture in LINE, Facebook and other apps.
- V12 | 2026-11-09 10:14 | Added a two-column layout on wide screens (upload on the left, results on the right) and an All Rights Reserved license.
- V11 | 2026-11-09 09:23 | Added a light/dark theme toggle in the top-right corner (dark by default, choice remembered).
- V10 | 2026-11-08 20:28 | Added search and social-sharing metadata (description, canonical link, Open Graph, structured data) and a more descriptive page title.
- V9 | 2026-11-07 15:03 | Fixed Android downloads so single files save as `.md` (not `.md.zip`); downloads go straight to the browser's normal download again.
- V8 | 2026-11-07 14:53 | Switched scanned-PDF OCR to Tesseract.js (Traditional Chinese + English) with sharper page rendering; downloads now use a save dialog in Chrome or the share sheet on Android when available.
- V7 | 2026-11-07 14:37 | Tried TrOCR (Hugging Face) for scanned-PDF OCR, with a warning that Chinese accuracy is limited.
- V6 | 2026-11-07 13:42 | Brought back PaddleOCR as the fallback for scanned PDFs.
- V5 | 2026-11-07 13:29 | Minor fixes: temporarily removed OCR while testing, briefly showed a "scanned PDF not supported" message, then returned to plain text-layer PDF extraction.
- V4 | 2026-11-07 13:05 | Switched the scanned-PDF OCR engine to PaddleOCR for better Chinese recognition.
- V3 | 2026-11-07 12:27 | Added OCR for scanned PDFs with no text layer (Tesseract.js, Traditional Chinese + English) with page-by-page progress, plus cleaner line breaks in PDF text.
- V2 | 2026-11-07 12:06 | Made downloads more reliable on phones, saved `.md` files as UTF-8 so Chinese text opens correctly, and added a message when there is nothing to download.
- V1 | 2026-11-07 11:31 | First public release: in-browser conversion of PDF, DOCX, PPTX, Excel, CSV/TSV, HTML, JSON, XML, TXT and MD to Markdown, with batch upload, preview, copy, per-file and ZIP download, and a Chinese/English toggle.
