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

Cette table est un résumé, **pas** l'inventaire juridique complet. Le setup fournit les textes et notices recensés dans `_internal/licenses/distribution/` du dossier d'installation, ainsi que des archives sources dans `sources/` sous ce répertoire. Les logiciels sous LGPL restent accessibles comme bibliothèques séparées et leurs droits de modification/remplacement sont préservés. La notice BSD de `proxy_tools` est ajoutée séparément, car sa wheel 0.1.0 ne contient pas de fichier de licence ; sa métadonnée MIT et son en-tête source BSD divergent et cette provenance est documentée dans le paquet.

Une archive source officielle de [Pandoc 3.9](https://hackage.haskell.org/package/pandoc-3.9) est préparée pour le paquet ; elle ne résout pas à elle seule la question juridique de son association à cette application propriétaire. Avant une distribution publique, la conformité de **tous** les composants du paquet, y compris les dépendances natives, doit être validée et explicitée dans les notes de Release.
