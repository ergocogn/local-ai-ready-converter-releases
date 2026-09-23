# Third-party components

[Lire en français](COMPOSANTS_TIERS.md) · [Home](../README.md)

Local AI-Ready Converter is proprietary/freeware for its original code. Bundled open-source software and the Microsoft runtime retain **their own licences and rights**. The product licence does not take those rights away.

| Component | Purpose | Main licence or terms |
| --- | --- | --- |
| [python-docx](https://github.com/python-openxml/python-docx) 1.2.0 | DOCX extraction | MIT |
| [Tesseract](https://github.com/tesseract-ocr/tesseract) and OCR models | Text recognition | Apache-2.0 and model-specific terms; native DLLs retain their own licences, including GPL/LGPL |
| [OCRmyPDF](https://github.com/ocrmypdf/OCRmyPDF) | Searchable PDF | MPL-2.0 |
| [pikepdf](https://github.com/pikepdf/pikepdf) | PDF processing used by OCRmyPDF | MPL-2.0 plus library notices |
| [fpdf2](https://github.com/py-pdf/fpdf2) and [img2pdf](https://gitlab.mister-muffin.de/josch/img2pdf) | PDF and images | LGPL-3.0 |
| [PyInstaller](https://github.com/pyinstaller/pyinstaller) | App launcher | GPL with bootloader exception |
| [Microsoft WebView2 Fixed Version](https://learn.microsoft.com/microsoft-edge/webview2/concepts/distribution) | Windows app window | Microsoft terms |
| [PySide6 / Qt](https://doc.qt.io/qtforpython-6/) | Linux app window | LGPL-3.0; bundled notices and corresponding-source information apply |
| [AppImage type2 runtime](https://github.com/AppImage/type2-runtime) | Self-contained Linux launcher | MIT; official signed static runtime |

This table is a summary, **not** the complete legal inventory. The Windows installer and Linux AppImage supply the collected notices and applicable source archives inside their package. LGPL components remain separately accessible libraries; their modification/replacement rights are preserved. A separate BSD notice for `proxy_tools` is included because its 0.1.0 wheel has no licence file; the discrepancy between MIT metadata and its BSD source header is documented in the package.

Pandoc is not in the 0.3.2 packages. The Windows OCR executables and DLLs match files in the official Tesseract 5.5.0 installer; the Linux AppImage contains its separately launched Tesseract 5.3.4 runtime. Native dependency inventories, notices, source archives and build information are shipped as applicable. The app runs Tesseract as a separate executable; its code is not incorporated into the proprietary conversion engine. This summary does not replace the full licence texts shipped with each package.
