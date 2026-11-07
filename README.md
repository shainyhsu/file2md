# Forest MD Converter

Convert common office and text files to Markdown in the browser. Batch-friendly. Files never leave your device.

**Live demo:** https://shainyhsu.github.io/file2md/

## Supported formats

| Type | Formats |
|------|---------|
| Documents | PDF, DOCX, PPTX |
| Spreadsheets | XLSX, XLS, CSV, TSV |
| Text | HTML, TXT, MD, JSON, XML |

- **PDF:** extract the text layer when present; otherwise OCR with Tesseract.js (Traditional Chinese + English)
- **DOCX:** mammoth → Markdown
- **PPTX:** slide text extraction
- **Excel:** each sheet becomes a Markdown table

## How to use

1. Open the site
2. Drop or select one or more files
3. Preview, copy, or download `.md`; use “download all as ZIP” for a batch

Language toggle (Traditional Chinese / English) is the globe icon in the top-right corner.

## Tech

- mammoth, SheetJS, PDF.js, JSZip, Turndown, Tesseract.js
- Inspired by Microsoft MarkItDown, implemented entirely client-side
- Hosted on GitHub Pages

## Notes

OCR quality on scanned PDFs depends on image clarity and fonts. Proofread important documents.
