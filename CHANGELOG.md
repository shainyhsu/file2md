# File to Markdown: changelog

Newest first. Each update of the page is one version. Times are Taiwan time (UTC+8).

- V17 | 2026-11-13 09:36 | Added a classic favicon.ico tab icon for older browsers and search tools.
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
