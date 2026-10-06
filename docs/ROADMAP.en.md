# Roadmap

[Lire en français](ROADMAP.md) · [Home](../README.md)

**Status, not a date promise.** Versions 0.1, 0.2 and 0.3 were development milestones. Windows 0.3.1 was the first public Release; version 0.3.3 is published for Windows and Linux. It improves the structure of image conversions. macOS remains planned; the announced next work is output quality, then AI-ready structure and local interoperability.

```mermaid
flowchart TB
  A["0.1–0.2<br/>local engine · OCR · batch"] --> B["0.3.1 Windows<br/>UI · walkthrough · per-file formats"]
  B --> C["Windows 0.3.1 validation<br/>conversions · installer"]
  C --> D["Windows Release<br/>setup · notices · checksums"]
  D --> U["Windows live update<br/>GitHub detection · verified download · upgrade"]

  D --> L["Linux 0.3.2<br/>native tools · AppImage · clean-VM tests"] --> S["Images 0.3.3<br/>logical structure · JSON/Markdown/TXT"]
  S --> UL["Linux 0.3.2 → 0.3.3 update<br/>download and package verified"]
  S --> W["Smart App Control compatibility<br/>Windows signing needed"]
  L --> M["macOS<br/>native tools · build · tests"]
  S --> Q["Output quality<br/>PDF/tables · errors · possible auto choice"]
  Q --> F["AI-ready folder<br/>ID · manifest · metadata · assets"]
  F --> P["Local interoperability<br/>API/MCP · permissions · reuse"]
  P --> K["Local retrieval<br/>chunks · embeddings · index"] --> R["Local RAG<br/>sourced passages · answers"]

  classDef done fill:#e9f5ef,stroke:#287451,color:#173f2e
  classDef active fill:#fff4dd,stroke:#a56b00,color:#553600
  classDef future fill:#f6f6f6,stroke:#666,color:#222
  class A,B,C,D,U,L,S done
  class UL,W active
  class M,Q,F,P,K,R future
```

**Green:** delivered and checked. **Amber:** validation in progress. **Grey:** not built yet. After the Windows and Linux platforms, the announced next work is output quality, then the AI-ready folder and local interoperability. macOS remains planned, with no announced order of passage: the port follows its own pace and does not gate that work.

| Stage | Actual status | Completion criterion |
| --- | --- | --- |
| **0.1–0.2 — foundation** | Conversion engine, OCR, batch handling, interface and initial destinations developed. | Historical milestones, not a current public offering. |
| **0.3 / 0.3.1 — Windows** | UI, walkthrough, per-file formats, session results and configurable links. | First Windows version published with installer and verified conversion/OCR. |
| **First Windows Release** | 0.3.1 in a separate distribution repository, without proprietary source. | Installer, bilingual notes, third-party notices and sources, checksum. The development repository remains private. |
| **Update verification** | Windows completed upgrades from 0.3.1 to 0.3.2 and from 0.3.2 to 0.3.3. On Linux, the 0.3.2 updater code detected and downloaded the public 0.3.3 release with checksum verification; the downloaded package launched and passed diagnostics. | The mechanism is delivered. The complete Linux graphical update flow still needs verification. |
| **Linux 0.3.2–0.3.3** | Native x86_64 AppImages are published. Conversions, OCR, searchable PDF and the PySide6/Qt window passed on Ubuntu Desktop 24.04; the downloaded 0.3.3 package passed package and UI checks. | Packages, checksums and bilingual instructions are published. |
| **Images 0.3.3 — logical structure** | Generic ordered JSON blocks represent clear headings, lists, label/value associations, selected controls and ruled tables; Markdown and TXT also use the structure. Plain OCR remains the fallback when the structure is uncertain. | Shipped for Windows and Linux. CSV keeps its existing behavior: no artificial table is created for a non-tabular image. |
| **Windows Smart App Control compatibility** | The public 0.3.2 and 0.3.3 setups are unsigned and may be blocked by this protection before launch. The 0.3.3 setup passed an upgrade and a fresh install on Windows where it was allowed to run. | Obtain a valid code signature, sign the Windows package and validate the final setup on a system enforcing this protection before claiming compatibility. |
| **macOS** | No macOS package validated. Planned, with no announced order of passage. | Build on macOS with compatible tools; handle signing/notarization if required for the chosen distribution route; test UI and conversion/OCR on a clean machine. Verify its update route. |
| **Quality / possible 0.4 cycle** | Intended, not promised for the first Release. | Better errors, complex tables/PDFs and compact tabular JSON; define any automatic-output mode explicitly, then test its rules. |
| **AI-ready structure** | Not implemented yet. | Stable folder, document ID, versioned JSON manifest, provenance, produced files, OCR/language, source format and organized assets. |
| **Local interoperability** | Not implemented yet. | Explicit local API and/or MCP to list documents, retrieve TXT/Markdown/JSON and identify existing conversions without repeated OCR. Permissions and no default network sharing. |
| **Local retrieval** | Not implemented yet. | Source-aware chunks, local embeddings and index, semantic search tested on a corpus. |
| **Local RAG** | Not implemented yet. | Questions over documents answered with relevant retrieved passages and verifiable references; gradual integration with different agents/AIs. |

The intended path is **document → local conversion → open formats → AI-ready folder → manifest → API/MCP → chunks → embeddings/index → retrieval → RAG**. Today's dated output folder is only a destination, **not yet** the standardized AI-ready folder. Version numbers for AI-ready/RAG stages will be decided when scope and tests are defined. See the [AI-ready explanation](AI_READY.en.md) and [architecture](ARCHITECTURE.en.md).

For discoverability, the repository description is “Local desktop document converter: PDF OCR, DOCX to Markdown, XLSX to CSV/JSON. Private by design; no account or command line.” Topics: `document-converter`, `pdf-ocr`, `local-first`, `batch-conversion`, `desktop-app`, `privacy`, `markdown`, `json`, `tesseract`, `ocrmypdf`, `windows`, `linux`. Do not use `open-source`: the application source is not published.
