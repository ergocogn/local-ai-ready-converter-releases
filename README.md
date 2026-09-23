# Local AI-Ready Converter

<p align="center"><img src="docs/assets/app-icon.png" width="110" alt="Local AI-Ready Converter icon"></p>

<p align="center"><strong>Turn documents into reusable files — on your own computer.</strong><br>Prepare them once. Choose how to use them next.</p>

<p align="center">Local · Freeware · No account · Batch conversion · No command line</p>

<p align="center"><a href="README.fr.md">Lire en français</a></p>

<p align="center">
  <a href="../../releases"><img src="docs/assets/windows-releases.svg" alt="Windows 11 x64 releases"></a>
  <img src="https://img.shields.io/badge/Linux-Coming_soon-d4d4d8?style=for-the-badge&amp;logo=linux&amp;logoColor=18181b" alt="Linux coming soon; no download yet">
  <img src="https://img.shields.io/badge/macOS-Coming_soon-d4d4d8?style=for-the-badge&amp;logo=apple&amp;logoColor=18181b" alt="macOS coming soon; no download yet">
</p>

> **Windows 0.3.1 is the first public release.** Download its installer from [Releases](../../releases). This repository contains distribution material, not the proprietary development source. Linux and macOS packages are planned, but are not available yet.

## A file you can read is not always a file you can reuse

A PDF invoice, a scanned letter, a Word report and an Excel workbook were made primarily for people to view. A script, a document search tool or an AI assistant often needs extracted text or structured data instead. Local AI-Ready Converter handles that preparation through a desktop interface: add files or folders, select compatible output formats, convert, and open the results in Explorer. **Your original documents are not modified.**

In practical terms, this is a **local document converter for PDF OCR, PDF to text/Markdown/JSON, DOCX to Markdown, XLSX to CSV/JSON, and image OCR**. It brings these jobs together in one graphical batch workflow.

No Python or Tesseract installation is required separately for the intended Windows package. You do not need an account or a command line to use the application. Conversion runs on your computer; document contents are not sent to an ergoCogn conversion service.

## See it in action

![The Windows interface showing converted sample documents](docs/assets/interface-demo.png)

*The screenshot shows a real conversion of synthetic PDF, CSV and XLSX test documents in an interface preview. No user document was used. [Generated output names and checksums](docs/assets/conversion-demo.json). The [About and support preview](docs/assets/about-demo-fr.png) shows the current French wording.*

## Why prepare documents locally?

- **Choose the useful representation.** Extract text from a PDF, OCR a scan, make a CSV per spreadsheet sheet, or convert a Word document to Markdown. Use JSON when structured data or page references matter.
- **Reuse the work.** Keep the converted output for later processing rather than repeating extraction or OCR every time another tool needs it.
- **Stay in control.** Select entire folders or individual files, filter by type, and choose outputs per batch or per compatible file. Results remain visible across conversions in the same session.
- **Keep your options open.** Use the outputs with a local AI, an online AI *if you choose to send them*, a script, a knowledge base or no AI at all.

This app prepares documents; **it does not include a generative AI model, semantic search, a local API/MCP server or RAG today.** The [roadmap](docs/ROADMAP.en.md) distinguishes these later stages from what already works.

## Proven tools, one visual workflow

This is not a replacement for every underlying converter. The app brings established tools together, handles files and destinations, runs batch jobs and presents the outputs without requiring the user to operate each tool separately. **python-docx** extracts DOCX text and structure; **Tesseract** and **OCRmyPDF** provide OCR and searchable PDFs; **pypdf** extracts text from text PDFs; **openpyxl** reads Excel workbooks. The Windows interface uses **pywebview and Microsoft WebView2**. These components keep their own licences and conditions: see the [third-party component summary](docs/COMPOSANTS_TIERS.en.md).

## Download and availability

| Platform | Status |
| --- | --- |
| Windows 11 x64 | Installer available from [Releases](../../releases). |
| Linux | Native build and testing planned after Windows. |
| macOS | Native build and testing planned after Linux. |

Get the Windows installer from [Releases](../../releases), check its [SHA-256 checksum](SHA256SUMS.txt), and follow the [installation and update guide](docs/INSTALLATION.en.md). The package includes its conversion tools and base OCR languages; you need not install them separately.

## Convert once. Reuse where it helps.

For example, a converted PDF may give you several views of the same source:

```text
report.pdf                 original, unchanged
report-Converted.txt       plain text
report-Converted.md        Markdown
report-Converted.json      structured output
```

The app can put outputs beside the source, in a dated conversion folder, or in a chosen destination. If a name already exists, it numbers the new output instead of overwriting the previous one. A second run can convert only newly requested formats for an unchanged source rather than needlessly repeating the same work in that session.

“AI-ready” means **prepared for a later tool**, not “AI is running inside this app”. You decide whether to keep the output local, send it to a service, or use it without AI. Open TXT, Markdown, CSV and JSON avoid locking the result into this converter.

## Supported inputs and outputs

| Input | Available outputs |
| --- | --- |
| Text PDF | TXT, Markdown, JSON; searchable PDF if explicitly selected |
| Scanned PDF | TXT, Markdown, JSON, searchable PDF via OCR |
| DOCX | TXT, Markdown, JSON |
| XLSX | JSON, one CSV per sheet |
| CSV | JSON |
| PNG, JPEG, TIFF | TXT, Markdown, JSON via OCR |

TXT suits straightforward text reuse. Markdown can preserve useful lightweight document structure. CSV is often the most economical view of a table. JSON is convenient when a program needs explicit structure, metadata or page boundaries; it can also be more verbose than CSV, especially for spreadsheets. **No format saves tokens automatically.** Choose the output for the next task. See the [usage guide](docs/UTILISATION.en.md) and [architecture](docs/ARCHITECTURE.en.md).

Automatic conversion is not infallible. OCR, complex tables, formulas and unusual PDF layouts can introduce omissions or errors. For important figures or decisions, check the result against the original.

## Privacy: local conversion, with clear network boundaries

Reading documents, OCR and writing converted files happen on your machine. There is no requirement to upload invoices, contracts or internal reports to a conversion website. A local AI workflow can keep both source and prepared output on your computer.

**“Local” does not mean “the app never accesses the Internet.”** A manual update check, publisher information from GitHub, a support link, or an OCR-language download you request can use the network. Windows WebView2 also has its own runtime behavior. None of these features is needed to send document contents to a remote conversion service. If your chosen output directory is synchronized by OneDrive or another provider, that synchronization is outside the converter's local processing. Read the [privacy and network explanation](docs/CONFIDENTIALITE.en.md).

## 🍃 Save tokens. Save energy. Use AI cleverly.

This is a working principle, **not a promise of a measured token or energy saving for every file**.

**Save tokens:** sending a whole PDF directly to a model API can be expensive in context. For example, [OpenAI's PDF file-input processing](https://developers.openai.com/api/docs/guides/file-inputs) may include both extracted text **and page images**. If your task only needs the words, sending the locally extracted TXT—or just the relevant pages—instead can substantially reduce the material processed and the associated input-token cost. A CSV for one spreadsheet sheet can likewise be much smaller than a verbose workbook JSON. Keep the original PDF when page images, layout or charts are essential. The actual saving depends on the document, model and API; the app does not measure or guarantee a percentage.

**Save energy:** keep and reuse a suitable conversion instead of rerunning extraction or OCR for every later question. A single file may yield a tiny difference; repeated processing across a collection may matter more. The app does not claim a quantified environmental benefit.

**Use AI cleverly:** prepare first, select what is relevant, then use the AI that suits your task—or none. This is the longer-term path toward documented AI-ready folders, local interoperability and retrieval; those capabilities are [planned, not currently shipped](docs/ROADMAP.en.md). [Read the full explanation](docs/AI_READY.en.md).

## Documentation

[Installation and updates](docs/INSTALLATION.en.md) · [Using the app](docs/UTILISATION.en.md) · [Privacy](docs/CONFIDENTIALITE.en.md) · [AI-ready vision](docs/AI_READY.en.md) · [Architecture](docs/ARCHITECTURE.en.md) · [Roadmap](docs/ROADMAP.en.md) · [Release notes](CHANGELOG.md)

## Help and support

Use this repository's [Issues](../../issues) to report a problem; please never attach confidential documents. You can [give the project a GitHub star](../../), which is free. Financial support is optional through [Stripe](https://buy.stripe.com/8x214pgIZ7ho3vUftg1oI00) and is **not** needed to use the free application. Other payment buttons are hidden until their URLs are configured. The in-app support area can be hidden in Settings. See [support and announcements](docs/SOUTIEN.en.md).

Local AI-Ready Converter is published by **ergoCogn sàrl**. This repository is for binary distribution, documentation, release notes and issue tracking; it does not publish the proprietary source. Read the [French reference licence](LICENSE.fr.md), its [English translation](LICENSE.en.md) and the [third-party component notices](docs/COMPOSANTS_TIERS.en.md). The Windows setup was tested offline in a clean Windows Sandbox.

<p align="center"><strong>Convert once. Reuse where it helps.</strong><br>🍃 Save tokens. Save energy. Use AI cleverly.</p>
