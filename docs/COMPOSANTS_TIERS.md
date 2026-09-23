# Composants tiers

[Read in English](COMPOSANTS_TIERS.en.md) · [Accueil](../README.fr.md)

Local AI-Ready Converter est distribué sous une licence propriétaire/freeware pour son code original. Les logiciels libres et le runtime Microsoft intégrés restent soumis à **leurs propres licences**. La licence du produit ne limite pas les droits que celles-ci vous donnent.

| Composant | Utilisation | Licence ou conditions principales |
| --- | --- | --- |
| [Pandoc](https://github.com/jgm/pandoc/releases/tag/3.9) 3.9 | Conversion DOCX | GPL-2.0-or-later |
| [Tesseract](https://github.com/tesseract-ocr/tesseract) et modèles OCR | Reconnaissance de texte | Apache-2.0 et licences des modèles |
| [OCRmyPDF](https://github.com/ocrmypdf/OCRmyPDF) | PDF recherchable | MPL-2.0 |
| [pikepdf](https://github.com/pikepdf/pikepdf) | Traitement PDF utilisé par OCRmyPDF | MPL-2.0 et notices de ses bibliothèques |
| [fpdf2](https://github.com/py-pdf/fpdf2) et [img2pdf](https://gitlab.mister-muffin.de/josch/img2pdf) | PDF et images | LGPL-3.0 |
| [PyInstaller](https://github.com/pyinstaller/pyinstaller) | Lanceur de l'application | GPL avec exception pour le bootloader |
| [Microsoft WebView2 Fixed Version](https://learn.microsoft.com/microsoft-edge/webview2/concepts/distribution) | Fenêtre de l'application Windows | Conditions Microsoft |

Cette table est un résumé, **pas** l'inventaire juridique complet. Le setup fournit les textes, mentions de copyright et licences de toutes les dépendances redistribuées dans `_internal/licenses/distribution/` du dossier d'installation. Les logiciels sous LGPL restent accessibles comme bibliothèques séparées et leurs droits de modification/remplacement sont préservés.

La source correspondante de Pandoc 3.9 est indiquée sur sa [page de version](https://github.com/jgm/pandoc/releases/tag/3.9). Avant une distribution publique, l'accès aux sources correspondantes des composants concernés et la conformité du paquet doivent être validés et explicités dans les notes de Release.
