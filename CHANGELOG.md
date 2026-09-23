# Release notes

[Lire en français](CHANGELOG.fr.md) · [Home](README.md)

## 0.3.1 — first Windows release (23 September 2026)

- Conversion UI organized around source files and results kept across batches.
- First-run walkthrough, type filter, selection and per-file output formats.
- Source-based `-Converted` output names, without overwriting existing files.
- Searchable PDF selectable as an output; Windows-1252 CSV input supported.
- Manual GitHub update check and installer download with size and SHA-256 verification.
- Optional Stripe support link and French/English GitHub star and Stripe labels.
- Self-contained Windows 11 x64 setup with bundled conversion tools, OCR and third-party notices/sources. Tested offline in a clean Windows Sandbox: installation, conversions/OCR, WebView2 startup and uninstallation.

Download `LocalAIReadyConverter-0.3.1-Setup.exe` from [Releases](../../releases) and verify its checksum in [SHA256SUMS.txt](SHA256SUMS.txt). Do not uninstall an older version first; close the app and run the new setup.
