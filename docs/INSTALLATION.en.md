# Install and update on Windows

[Lire en français](INSTALLATION.md) · [Home](../README.md)

## Install

1. Use Windows 11 x64.
2. Once a public package exists, download `LocalAIReadyConverter-X.Y.Z-Setup.exe` from [Releases](../../../releases).
3. Run it and follow the graphical installer. Installation is for your Windows account.
4. Open **Local AI-Ready Converter** from the Start menu or at the end of setup.

Do not download a `.incomplete` or `.part` file. Conversion tools and basic OCR languages are included; you do not need to install Python or Tesseract separately on the user machine. No command line is needed to use the app.

## Update

In **Settings → Updates**, check on demand. If a newer Release exists with a compatible Windows installer, the app can download and verify the setup, then reveal it in Explorer. It does not run or install the setup silently.

Close the app, then run the newer setup. **Do not uninstall the old version first**: setup upgrades it. Your documents are not managed by the installer, and user preferences are kept. A real public-Release update check has not yet been completed because this distribution repository is still private; the update code has been tested with simulated GitHub responses.

## Uninstall

Use **Windows Settings → Installed apps → Local AI-Ready Converter → Uninstall**. This removes the app, not your documents or converted files.

If setup or update fails, close all app windows and retry. Once Issues are public, [report a problem](../../../issues) with your Windows and app versions and the error message, but do not attach confidential documents.
