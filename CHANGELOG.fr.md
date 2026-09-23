# Notes de version

[Read in English](CHANGELOG.md) · [Accueil](README.fr.md)

## 0.3.1 — première version Windows (23 septembre 2026)

- Interface organisée autour des fichiers à convertir et des résultats conservés entre lots.
- Assistant de découverte, filtre par type, sélection et formats ajustables par fichier.
- Nommage des sorties d'après l'original avec `-Converted`, sans écrasement.
- PDF recherchable par OCR sélectionnable comme sortie ; CSV Windows-1252 pris en charge en entrée.
- Vérification manuelle des mises à jour GitHub et téléchargement de l'installateur avec contrôle de taille et de SHA-256.
- Lien de soutien Stripe facultatif et libellés étoile GitHub/Stripe en français et anglais.
- Setup autonome Windows 11 x64 avec outils de conversion, OCR, notices et sources tierces intégrés. Testé hors ligne dans un Windows Sandbox propre : installation, conversions/OCR, démarrage de WebView2 et désinstallation.

Téléchargez `LocalAIReadyConverter-0.3.1-Setup.exe` dans les [Releases](../../releases) et vérifiez son empreinte dans [SHA256SUMS.txt](SHA256SUMS.txt). Ne désinstallez pas une ancienne version : fermez l'application et lancez le nouveau setup.
