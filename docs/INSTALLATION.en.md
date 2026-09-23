# Install and update

[Lire en français](INSTALLATION.md) · [Home](../README.md)

## Windows 11 x64

1. Download `LocalAIReadyConverter-X.Y.Z-Setup.exe` from [Releases](../../../releases).
2. Run it and follow the graphical installer. Installation is for your Windows account.
3. Open **Local AI-Ready Converter** from the Start menu or at the end of setup.

Do not download a `.incomplete` or `.part` file. The setup includes the conversion tools and base OCR languages; you do not need to install Python or Tesseract separately. No command line is needed.

To update, close the app and run the newer setup. **Do not uninstall the old version first**: setup upgrades it. User preferences are kept, and the installer does not manage your documents. To uninstall, use **Windows Settings → Installed apps → Local AI-Ready Converter → Uninstall**.

## Linux x86_64

1. Download `LocalAIReadyConverter-X.Y.Z-Linux-x86_64.AppImage` from [Releases](../../../releases).
2. In your file manager, open **Properties → Permissions** and allow the file to run as a program.
3. Double-click the AppImage.

The AppImage is portable: it does not need a system-wide installation. It was validated on a clean Ubuntu Desktop 24.04 VM and includes Python, Tesseract, the base OCR languages and a modern static AppImage runtime; `libfuse2` is not required. To remove it, delete the AppImage. Your source documents and converted files are not removed.

## Updates

In **Settings → Updates**, check on demand. If a newer Release contains a compatible native package, the app downloads it, verifies its size and SHA-256 digest, and reveals it in the file manager. It never runs or installs the package silently.

On Windows, close the app and run the downloaded setup. On Linux, close the app and open the downloaded AppImage; the app marks it executable after a verified download. Installation of an update remains a manual, visible action.

If setup, startup or update fails, close all app windows and retry. [Report a problem](../../../issues) with your operating system, app version and the exact error message, but never attach confidential documents.
