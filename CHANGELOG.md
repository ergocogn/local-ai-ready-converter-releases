# Release notes

[Lire en français](CHANGELOG.fr.md) · [Home](README.md)

## 0.3.2 — cancellation reliability update (23 September 2026)

- Stop an active conversion immediately, including its external OCR process tree.
- Allow the application window to close safely while a conversion is being stopped.
- Show a compact Stop icon during processing, with an accessible tooltip.
- Report OneDrive or other Windows cloud files that are still online-only instead of silently triggering a long hydration during a batch.
- Keep cancellations distinct from conversion failures in the result list.
- Add the first self-contained Linux x86_64 AppImage, using the same conversion engine and PySide6/Qt desktop interface.
- Bundle Python, Tesseract, OCR languages and a signed static AppImage runtime; no separate Python, Tesseract or `libfuse2` installation is required.
- Validate the AppImage directly on a clean Ubuntu Desktop 24.04 VM: startup, DOCX/PDF/CSV/XLSX/image/TIFF conversion, multilingual OCR and searchable PDF.

This is the recommended Windows and Linux release. On Windows, close version 0.3.1 and run `LocalAIReadyConverter-0.3.2-Setup.exe`; uninstalling first is not required. On Linux x86_64, download the AppImage, allow it to run as a program in file properties, then double-click it.

## 0.3.1 — first Windows release (23 September 2026)

- Conversion UI organized around source files and results kept across batches.
- First-run walkthrough, type filter, selection and per-file output formats.
- Source-based `-Converted` output names, without overwriting existing files.
- Searchable PDF selectable as an output; Windows-1252 CSV input supported.
- Manual GitHub update check and installer download with size and SHA-256 verification.
- Optional Stripe support link and French/English GitHub star and Stripe labels.
- Self-contained Windows 11 x64 setup with bundled conversion tools, OCR and third-party notices/sources. Tested offline in a clean Windows Sandbox: installation, conversions/OCR, WebView2 startup and uninstallation.

Download `LocalAIReadyConverter-0.3.1-Setup.exe` from [Releases](../../releases) and verify its checksum in [SHA256SUMS.txt](SHA256SUMS.txt). Do not uninstall an older version first; close the app and run the new setup.
