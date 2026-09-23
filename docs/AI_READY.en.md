# Save tokens. Save energy. Use AI cleverly.

[Lire en français](AI_READY.md) · [Home](../README.md)

## The idea in one sentence

Prepare a document once, then reuse **the right information in the right format**, instead of repeatedly passing the entire raw file through a chain of tools.

A scanned PDF may be an image with no selectable text. A spreadsheet may contain several sheets, formulas and empty cells. A Word document can mix headings, tables and paragraphs. Before an AI tool or search engine can use that content, someone often has to extract a simpler representation. Local AI-Ready Converter performs this **preparation step on your computer**; it does not choose an AI provider for you.

## “Save tokens”: less irrelevant context, not magic

A *token* is a unit processed by a language model. Cost, speed and available context partly depend on how many tokens you send. **Sending a PDF directly to an API is a concrete case:** [OpenAI's API can include both extracted text and page images in its PDF input](https://developers.openai.com/api/docs/guides/file-inputs). If you only need to find an amount or summarize text, extracting TXT locally and sending just the useful passage can substantially reduce context and its cost. That is not equivalent when the AI needs to see layout, an image or a chart.

For a spreadsheet, one sheet's CSV may be much smaller than JSON describing every empty cell. Conversely, JSON can be useful when page numbers, formulas or detailed structure matter.

**A practical example:** convert a workbook to CSV and JSON. To ask an agent “which rows match product X?”, send only the relevant CSV sheet. To audit a formula, use the JSON. Choose the representation for the question; there is no universal “AI format”.

Conversion alone does not automatically save tokens. If you send **every** output to a model, you may use more. The current app neither counts tokens saved nor selects passages to send for you.

## “Save energy”: avoid repeated work, without a numerical promise

OCR, document parsing and AI requests use computing resources. Keeping a reusable TXT, Markdown, JSON or CSV result may avoid repeating the same extraction for each question. A local batch also prepares many files in one workflow. But conversion itself uses energy on your computer, and any overall gain depends on what happens next. **We do not claim measured energy savings for every file.** The motto states a design goal: avoid unnecessary repeated processing.

## “Use AI cleverly”: keep choice and provenance

You can inspect a prepared output **before** giving it to an agent. Share only an excerpt, choose TXT for reading, JSON for page references, CSV for tables, or keep everything local and never use AI at all. Originals stay intact; the new files remain under your control. OCR and PDF extraction do not guarantee accuracy: check important amounts, names and tables.

Document conversion is local, but optional features use the network and the Windows runtime has its own behaviour. The [privacy page](CONFIDENTIALITE.en.md) separates these aspects; “local” does not mean “no possible connection”.

## What exists — and what comes later

Today: visual import, local conversion, OCR, open outputs, format and destination selection. There is **no** built-in vector database, semantic search, API/MCP server or RAG.

The intended path is incremental: a stable AI-ready folder and a JSON manifest of completed work; explicit local API/MCP access so OCR and parsing need not be repeated; then chunking, local embeddings and an index; finally semantic retrieval and local RAG with passage citations. Each stage should preserve document control and be tested on its own. See the [roadmap](ROADMAP.en.md) and [architecture](ARCHITECTURE.en.md).
