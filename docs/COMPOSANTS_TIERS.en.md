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

This table is a summary, **not** the complete legal inventory. The installer supplies third-party licence texts, copyright notices and notices in `_internal/licenses/distribution/`. LGPL components remain separately accessible libraries; their modification/replacement rights are preserved.

Pandoc 3.9's corresponding source is identified on its [release page](https://github.com/jgm/pandoc/releases/tag/3.9). Before public distribution, access to the corresponding sources of applicable components and compliance of the exact package need to be validated and described in release notes.
