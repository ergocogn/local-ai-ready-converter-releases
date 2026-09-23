# Third-party components

[Lire en français](COMPOSANTS_TIERS.md) · [Home](../README.md)

Local AI-Ready Converter is proprietary/freeware for its original code. Bundled open-source software and the Microsoft runtime retain **their own licences and rights**. The product licence does not take those rights away.

| Component | Purpose | Main licence or terms |
| --- | --- | --- |
| [Pandoc](https://github.com/jgm/pandoc/releases/tag/3.9) 3.9 | DOCX conversion | GPL-2.0-or-later |
| [Tesseract](https://github.com/tesseract-ocr/tesseract) and OCR models | Text recognition | Apache-2.0 and model-specific terms |
| [OCRmyPDF](https://github.com/ocrmypdf/OCRmyPDF) | Searchable PDF | MPL-2.0 |
| [pikepdf](https://github.com/pikepdf/pikepdf) | PDF processing used by OCRmyPDF | MPL-2.0 plus library notices |
| [fpdf2](https://github.com/py-pdf/fpdf2) and [img2pdf](https://gitlab.mister-muffin.de/josch/img2pdf) | PDF and images | LGPL-3.0 |
| [PyInstaller](https://github.com/pyinstaller/pyinstaller) | App launcher | GPL with bootloader exception |
| [Microsoft WebView2 Fixed Version](https://learn.microsoft.com/microsoft-edge/webview2/concepts/distribution) | Windows app window | Microsoft terms |

This table is a summary, **not** the complete legal inventory. The installer supplies the collected notices in `_internal/licenses/distribution/`, with source archives in its `sources/` subdirectory. LGPL components remain separately accessible libraries; their modification/replacement rights are preserved. A separate BSD notice for `proxy_tools` is included because its 0.1.0 wheel has no licence file; the discrepancy between MIT metadata and its BSD source header is documented in the package.

An official [Pandoc 3.9](https://hackage.haskell.org/package/pandoc-3.9) source archive is being prepared for the package; this alone does not settle the legal question of combining it with this proprietary application. Before public distribution, compliance of **all** packaged components, including native dependencies, must be checked and described in the Release notes.
