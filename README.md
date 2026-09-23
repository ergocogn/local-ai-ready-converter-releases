# Local AI-Ready Converter

**Vos documents, convertis chez vous. Prêts à être réutilisés où vous voulez.**

Une facture en PDF, un classeur Excel, un document Word ou un scan ne se prête pas toujours bien à la recherche et aux outils d'IA. Local AI-Ready Converter transforme ces fichiers sur votre ordinateur en texte et formats ouverts. Vous gardez la main sur les originaux, les sorties et leur destination — sans compte et sans service de conversion distant.

> Préparation de la distribution : ce dépôt est actuellement privé. Aucun téléchargement public n'est encore annoncé.

![Aperçu de l'application avec deux fichiers de démonstration](docs/assets/interface-demo.png)

*Aperçu de l'interface 0.3.1. Les fichiers montrés ont été créés pour cette capture ; aucune donnée d'utilisateur n'a été utilisée.*

## Télécharger et installer

La première distribution prévue est pour **Windows 11 x64**. Une fois publiée, téléchargez `LocalAIReadyConverter-X.Y.Z-Setup.exe` dans les [Releases](../../releases), puis lancez-le. Le programme embarque les outils nécessaires : Python, Pandoc ou Tesseract n'ont pas à être installés séparément. Pour mettre à jour, fermez l'application et lancez le nouveau setup **sans désinstaller l'ancien**.

Voir le [guide d'installation](docs/INSTALLATION.md). Linux et macOS sont prévus ensuite, mais aucun paquet pour ces systèmes n'est disponible aujourd'hui.

## Pourquoi cet outil ?

Parce qu'un fichier lisible à l'écran n'est pas forcément facile à exploiter. Un PDF scanné peut nécessiter de l'OCR ; un classeur contient plusieurs feuilles ; un document Word mélange texte et structure. Le convertisseur prépare des représentations plus simples à chercher, contrôler, archiver ou fournir à **l'outil de votre choix**. Il ne lance pas d'IA et ne crée pas encore d'index ou de RAG : il prépare les documents en amont.

La conversion locale a une conséquence concrète : **le contenu sélectionné est traité sur votre machine, et les sorties y sont écrites**. Vous n'avez pas à déposer vos documents chez un prestataire de conversion. Cela ne signifie pas « zéro réseau en toute circonstance » : vérifier les mises à jour, consulter le profil public GitHub, ouvrir un lien ou télécharger une langue OCR peut utiliser Internet. L'application n'envoie pas vos documents à ces services. Voir la [note de confidentialité et les limites du runtime Windows](docs/CONFIDENTIALITE.md).

## Comment ça marche

1. Glissez des fichiers ou un dossier, puis filtrez et cochez ce que vous voulez traiter.
2. Choisissez les sorties pour le lot, ou ajustez-les fichier par fichier ; la destination se règle dans Paramètres.
3. Lancez la conversion et ouvrez chaque résultat directement depuis la colonne de droite.

Les originaux restent intacts. Les nouveaux noms reprennent le nom source avec `-Converted` ; les collisions sont numérotées plutôt qu'écrasées. L'application garde les résultats de la session visibles entre plusieurs passages.

## Ce que l'application convertit

| Entrée | Sorties possibles |
| --- | --- |
| PDF textuel ou scanné | TXT, Markdown, JSON, PDF recherchable avec OCR |
| DOCX | TXT, Markdown, JSON |
| XLSX | JSON, un CSV par feuille |
| CSV | JSON |
| PNG, JPEG, TIFF | TXT, Markdown, JSON après OCR |

Le [guide d'utilisation](docs/UTILISATION.md) détaille les destinations, les conversions par lot, l'OCR et les limites connues.

## Pour quoi faire ensuite ?

Un TXT léger peut servir à retrouver une information ; un JSON de PDF conserve la séparation par page ; un CSV par feuille facilite l'analyse d'un classeur. Ces fichiers peuvent être relus, vérifiés et transmis ensuite à un outil d'IA **si vous le décidez**. La conversion n'est pas une garantie d'exactitude : contrôlez les chiffres, les tableaux et le texte OCR avant un usage important. Notre [vision AI-ready](docs/AI_READY.md) explique aussi les étapes futures, distinctes de ce qui existe déjà.

## Aide et évolution

- [Signaler un problème ou proposer une amélioration](../../issues) — disponible après l'ouverture publique du dépôt.
- [Notes de version](CHANGELOG.md)
- [Fonctionnement et architecture](docs/ARCHITECTURE.md)
- [Pourquoi « Save tokens. Save energy. Use AI cleverly. » ?](docs/AI_READY.md)
- [Feuille de route publique](docs/ROADMAP.md)
- [Licence du produit](LICENSE.md) et [composants tiers](docs/COMPOSANTS_TIERS.md)

Si le projet vous est utile, vous pourrez aussi lui donner une étoile sur GitHub. Les liens de soutien financier n'apparaîtront que lorsqu'ils seront réellement configurés ; aucun paiement n'est intégré à l'application.
L'[espace de soutien et d'annonces](docs/SOUTIEN.md) est facultatif et peut être masqué.

Local AI-Ready Converter est édité par **ergoCogn sàrl**. Ce dépôt est réservé à la distribution, aux notes de version et à l'aide ; le code source propriétaire de l'application n'y est pas publié.
