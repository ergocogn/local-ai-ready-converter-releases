# Notes de version

[Read in English](CHANGELOG.md) · [Accueil](README.fr.md)

## 0.3.3 — conversion structurée des images (6 octobre 2026)

- Ajout de blocs génériques ordonnés par page au JSON des images, sans supprimer le texte OCR ni les champs existants.
- Reconnaissance prudente des titres, listes, paires libellé/valeur, contrôles sélectionnés et tableaux à grille visible, sans modèle propre à un type de document.
- Utilisation des structures fiables en Markdown et TXT ; repli sur le texte OCR si la disposition est incertaine.
- CSV reste indisponible pour les images ; les autres formats d'entrée conservent leurs sorties.

**Mise à jour du paquet 0.3.3 — 6 octobre 2026 :** l'installateur Windows a été reconstruit sans changer de numéro. Cette révision récupère plus prudemment le début des textes clairs sur fond sombre, empêche les lignes techniques TSV de contaminer les sorties, rattache les annotations intercalées aux éléments visuels et ajoute au JSON les observations génériques `selected` et `highlighted` tout en conservant le champ `state`. Markdown garde son rendu existant et TXT bénéficie de séparations et d'indentations plus stables. L'AppImage Linux publiée sous le même numéro n'est pas remplacée par cette mise à jour Windows.

L'OCR et le regroupement visuel restent approximatifs. Vérifiez les valeurs et relations importantes sur l'image originale.

Le **JSON des images est la principale amélioration** : `pages[].blocks` représente les éléments dans l'ordre de lecture, avec des types génériques, des éléments imbriqués, des associations libellé/valeur et des états visuels lorsqu'ils sont détectés avec suffisamment de confiance. Les champs OCR `text` et `pages[].text` restent disponibles. Ce JSON décrit la structure visible de chaque image ; il ne constitue pas encore un manifest AI-ready pour toute la bibliothèque de documents.

**Compatibilité Windows :** l'installateur 0.3.3 n'est pas signé. Un Windows appliquant Smart App Control peut le bloquer avant le début de l'installation. La même restriction concerne l'installateur 0.3.2 non signé. Voir le [guide d'installation](docs/INSTALLATION.md).

## 0.3.2 — fiabilisation de l’arrêt (23 septembre 2026)

- Arrêt immédiat d’une conversion active, y compris l’arbre des processus OCR externes.
- Fermeture sûre de la fenêtre pendant l’arrêt d’une conversion.
- Icône Stop compacte pendant le traitement, avec infobulle accessible.
- Signalement clair des fichiers OneDrive ou cloud Windows encore disponibles uniquement en ligne, sans lancer silencieusement un long téléchargement pendant le lot.
- Distinction entre une annulation et un échec de conversion dans les résultats.
- Première AppImage Linux x86_64 autonome, avec le même moteur de conversion et une interface de bureau PySide6/Qt.
- Python, Tesseract, langues OCR et runtime AppImage statique signé intégrés ; aucune installation séparée de Python, Tesseract ou `libfuse2` n'est requise.
- Validation directe de l'AppImage sur une VM Ubuntu Desktop 24.04 propre : démarrage, conversion DOCX/PDF/CSV/XLSX/images/TIFF, OCR multilingue et PDF recherchable.

Pour installer la 0.3.2 sous Windows depuis la 0.3.1, il suffisait de fermer l'application et de lancer `LocalAIReadyConverter-0.3.2-Setup.exe`, sans désinstallation préalable. Sous Linux x86_64, l'AppImage devait être autorisée à s'exécuter dans les propriétés du fichier.

## 0.3.1 — première version Windows (23 septembre 2026)

- Interface organisée autour des fichiers à convertir et des résultats conservés entre lots.
- Assistant de découverte, filtre par type, sélection et formats ajustables par fichier.
- Nommage des sorties d'après l'original avec `-Converted`, sans écrasement.
- PDF recherchable par OCR sélectionnable comme sortie ; CSV Windows-1252 pris en charge en entrée.
- Vérification manuelle des mises à jour GitHub et téléchargement de l'installateur avec contrôle de taille et de SHA-256.
- Lien de soutien Stripe facultatif et libellés étoile GitHub/Stripe en français et anglais.
- Setup autonome Windows 11 x64 avec outils de conversion, OCR, notices et sources tierces intégrés. Installation, conversions/OCR, démarrage de l'interface et désinstallation vérifiés hors ligne.

Téléchargez `LocalAIReadyConverter-0.3.1-Setup.exe` dans les [Releases](../../releases) et vérifiez son empreinte dans [SHA256SUMS.txt](SHA256SUMS.txt). Ne désinstallez pas une ancienne version : fermez l'application et lancez le nouveau setup.
