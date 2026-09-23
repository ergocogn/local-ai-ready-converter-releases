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
| [PySide6 / Qt](https://doc.qt.io/qtforpython-6/) | Fenêtre de l'application Linux | LGPL-3.0 ; notices et informations sur les sources correspondantes intégrées |
| [Runtime AppImage type2](https://github.com/AppImage/type2-runtime) | Lanceur Linux autonome | MIT ; runtime statique officiel signé |

Cette table est un résumé, **pas** l'inventaire juridique complet. Le setup Windows et l'AppImage Linux fournissent dans leur paquet les textes, notices et archives sources applicables. Les logiciels sous LGPL restent accessibles comme bibliothèques séparées et leurs droits de modification/remplacement sont préservés. La notice BSD de `proxy_tools` est ajoutée séparément, car sa wheel 0.1.0 ne contient pas de fichier de licence ; sa métadonnée MIT et son en-tête source BSD divergent et cette provenance est documentée dans le paquet.

Pandoc ne fait pas partie des paquets 0.3.2. Les exécutables et DLL OCR de Windows correspondent à l'installateur officiel Tesseract 5.5.0 ; l'AppImage Linux contient son runtime Tesseract 5.3.4 lancé séparément. Les inventaires des dépendances natives, notices, archives sources et informations de construction sont livrés selon le paquet. L'application communique avec Tesseract par lancement d'un exécutable séparé, sans intégrer son code dans le moteur propriétaire. Ce résumé ne remplace pas les licences complètes livrées avec chaque paquet.
