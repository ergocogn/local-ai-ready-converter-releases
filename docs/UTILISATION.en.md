# Using the app

[Lire en français](UTILISATION.md) · [Home](../README.md)

## Convert without a command line

Drop files or folders into the import area, or use the add buttons. **Files to convert**, on the left, groups the imported files. Filter by type, select the files you want and remove entries from the list without deleting the originals.

Select batch output formats at the top. The capsules on a file row let you adjust its formats; incompatible choices are disabled. Click **Convert** below the two columns. Completed results remain on the right between conversion runs. Click a result capsule to reveal the corresponding file in the file manager.

Running again without changes does not repeat outputs already produced in the session. Adding a format creates only the missing output. If a source or destination changes, another conversion may be needed. Existing output names are numbered rather than overwritten.

## Destination

In **Settings**, choose a dated `Conversion-YYYY-MM-DD` folder beside the sources, the same folder as each original, or one chosen destination folder. Originals remain untouched. Make sure the destination has enough free space and write access before a large batch.

## OCR

OCR recognizes text in images and scanned PDFs. **Searchable PDF** makes a new PDF with a text layer and can be the only selected output. Choose recognition languages in Settings. Basic languages come with the Windows package; additional models can be imported or downloaded on request.

## Choosing an output for AI

For a PDF, TXT is often lighter; JSON also retains page separation. For a tabular Excel workbook, one CSV per sheet is often more compact than detailed JSON. The JSON preserves more structure and formulas. A calculated value can be included only when the workbook stored it; the app does not recalculate Excel.

Text quality depends on the source. A PDF's text layer may be imperfect, and OCR cannot guarantee an exact transcript. Check sensitive details and important figures before reuse. The [AI-ready explanation](AI_READY.en.md) gives practical selection examples.
