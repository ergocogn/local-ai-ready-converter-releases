# Privacy: what stays local, what may use the Internet

[Lire en français](CONFIDENTIALITE.md) · [Home](../README.md)

**Your documents are converted on your computer.** The app reads the sources you choose, writes outputs to your chosen destination and does not send their contents to an AI or document-conversion service. No account or command line is required. Originals are not modified.

This describes **conversion**, not every feature of the app or Windows:

| Action | Network? | Your document contents? |
| --- | --- | --- |
| Convert a PDF, spreadsheet, CSV, DOCX or image with bundled tools | Not required for conversion | Read and written locally |
| Check for an update or open a GitHub page | Yes, when requested | Not sent by the app |
| Load public GitHub profile information in About | Yes, when that view opens, with an offline local fallback | Not sent |
| Download an additional OCR language | Yes, only when requested | Not sent |
| Follow a support or ad link | Your browser opens an external site | No document sent by the app; the site has its own privacy policy |

You can hide the support area in Settings. Any future ad is an image bundled with the package, not an image fetched from a server every time; no ad-network script is integrated today. See [support and ads](SOUTIEN.en.md).

**Windows runtime note:** the window uses bundled Microsoft Edge **WebView2 Fixed Version**. This runtime has its own terms and may have Microsoft network or protection features independent of conversion. Microsoft Defender SmartScreen is included and collects and sends end-user information to Microsoft under the [Microsoft privacy statement](https://aka.ms/privacy) and [SmartScreen white paper](https://learn.microsoft.com/en-us/microsoft-edge/privacy-whitepaper#smartscreen). This is not a deliberate document upload by the conversion engine. See the [WebView2 distribution documentation](https://learn.microsoft.com/microsoft-edge/webview2/concepts/distribution).

**Outputs may contain the same sensitive data** as originals, sometimes in an easier-to-read or search form. Choose a suitable destination, protect your backups and review important information before sharing it. Files stored in a folder synchronized by OneDrive or a similar service remain subject to that service's settings; the app does not control such syncing.

The package includes separately licensed components; their notices and required sources are described under [third-party components](COMPOSANTS_TIERS.en.md) and shipped with the installer.
