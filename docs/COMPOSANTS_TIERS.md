# Composants tiers

[Read in English](COMPOSANTS_TIERS.en.md) · [Accueil](../README.fr.md)

Local AI-Ready Converter est distribué sous une licence propriétaire/freeware pour son code original. Les logiciels libres et le runtime Microsoft intégrés restent soumis à **leurs propres licences**. La licence du produit ne limite pas les droits que celles-ci vous donnent.

| Composant | Utilisation | Licence ou conditions principales |
| --- | --- | --- |
| [python-docx](https://github.com/python-openxml/python-docx) 1.2.0 | Extraction DOCX | MIT |
| [Tesseract](https://github.com/tesseract-ocr/tesseract) et modèles OCR | Reconnaissance de texte | Apache-2.0 et licences des modèles ; ses DLL natives ont leurs propres licences, dont GPL/LGPL |
| [OCRmyPDF](https://github.com/ocrmypdf/OCRmyPDF) | PDF recherchable | MPL-2.0 |
| [pikepdf](https://github.com/pikepdf/pikepdf) | Traitement PDF utilisé par OCRmyPDF | MPL-2.0 et notices de ses bibliothèques |
| [fpdf2](https://github.com/py-pdf/fpdf2) et [img2pdf](https://gitlab.mister-muffin.de/josch/img2pdf) | PDF et images | LGPL-3.0 |
| [PyInstaller](https://github.com/pyinstaller/pyinstaller) | Lanceur de l'application | GPL avec exception pour le bootloader |
| [Microsoft WebView2 Fixed Version](https://learn.microsoft.com/microsoft-edge/webview2/concepts/distribution) | Fenêtre de l'application Windows | Conditions Microsoft |

Cette table est un résumé, **pas** l'inventaire juridique complet. Le setup fournit les textes et notices recensés dans `_internal/licenses/distribution/` du dossier d'installation, ainsi que des archives sources dans `sources/` sous ce répertoire. Les logiciels sous LGPL restent accessibles comme bibliothèques séparées et leurs droits de modification/remplacement sont préservés. La notice BSD de `proxy_tools` est ajoutée séparément, car sa wheel 0.1.0 ne contient pas de fichier de licence ; sa métadonnée MIT et son en-tête source BSD divergent et cette provenance est documentée dans le paquet.

Pandoc ne fait pas partie du paquet Windows 0.3.1. Les 73 exécutables et DLL OCR correspondent aux fichiers de l'installateur officiel Tesseract 5.5.0. Le dossier `tesseract/native/` contient un inventaire et les notices des dépendances natives ; `sources/` contient notamment les sources et recettes des composants GPL/LGPL, dont JBIG-KIT et le runtime GCC. L'application communique avec Tesseract par lancement d'un exécutable séparé, sans intégrer son code dans le moteur propriétaire. Ce résumé ne remplace pas les licences complètes livrées avec le setup.
