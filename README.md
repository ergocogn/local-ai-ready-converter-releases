# Local AI-Ready Converter

Convertissez vos documents sur votre ordinateur, sans compte et sans envoyer leur contenu à une IA distante. Local AI-Ready Converter produit des fichiers ouverts et réutilisables pour la recherche, l'analyse et les outils d'IA que vous choisissez.

> Préparation de la distribution : ce dépôt est actuellement privé. Aucun téléchargement public n'est encore annoncé.

## Télécharger et installer

La première distribution prévue est pour **Windows 11 x64**. Une fois publiée, téléchargez `LocalAIReadyConverter-X.Y.Z-Setup.exe` dans les [Releases](../../releases), puis lancez-le. Le programme embarque les outils nécessaires : Python, Pandoc ou Tesseract n'ont pas à être installés séparément. Pour mettre à jour, fermez l'application et lancez le nouveau setup **sans désinstaller l'ancien**.

Voir le [guide d'installation](docs/INSTALLATION.md). Linux et macOS sont prévus ensuite, mais aucun paquet pour ces systèmes n'est disponible aujourd'hui.

## Ce que l'application convertit

| Entrée | Sorties possibles |
| --- | --- |
| PDF textuel ou scanné | TXT, Markdown, JSON, PDF recherchable avec OCR |
| DOCX | TXT, Markdown, JSON |
| XLSX | JSON, un CSV par feuille |
| CSV | JSON |
| PNG, JPEG, TIFF | TXT, Markdown, JSON après OCR |

Choisissez les fichiers et les formats, puis lancez la conversion. Les originaux ne sont pas modifiés. Les résultats reçoivent le suffixe `-Converted` ; une nouvelle conversion ne remplace pas un fichier existant. Les formats incompatibles ne sont pas proposés pour un fichier.

Le [guide d'utilisation](docs/UTILISATION.md) détaille les destinations, les conversions par lot, l'OCR et les limites connues.

## Confidentialité et connexion

La conversion des documents se fait localement. L'application peut accéder au réseau **à votre demande** pour télécharger une langue OCR, vérifier une mise à jour ou afficher des informations publiques GitHub. Elle n'envoie pas vos documents à ces services. Le runtime Microsoft WebView2 intégré a ses propres conditions et fonctions réseau ; voir la [note de confidentialité](docs/CONFIDENTIALITE.md).

## Aide et évolution

- [Signaler un problème ou proposer une amélioration](../../issues) — disponible après l'ouverture publique du dépôt.
- [Notes de version](CHANGELOG.md)
- [Fonctionnement et architecture](docs/ARCHITECTURE.md)
- [Pourquoi « Save tokens. Save energy. Use AI cleverly. » ?](docs/AI_READY.md)
- [Feuille de route publique](docs/ROADMAP.md)
- [Licence du produit](LICENSE.md) et [composants tiers](docs/COMPOSANTS_TIERS.md)

Local AI-Ready Converter est édité par **ergoCogn sàrl**. Ce dépôt est réservé à la distribution, aux notes de version et à l'aide ; le code source propriétaire de l'application n'y est pas publié.
