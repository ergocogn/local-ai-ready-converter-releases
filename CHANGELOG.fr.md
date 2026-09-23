# Notes de version

[Read in English](CHANGELOG.md) · [Accueil](README.fr.md)

## 0.3.2 — fiabilisation de l’arrêt (23 septembre 2026)

- Arrêt immédiat d’une conversion active, y compris l’arbre des processus OCR externes.
- Fermeture sûre de la fenêtre pendant l’arrêt d’une conversion.
- Icône Stop compacte pendant le traitement, avec infobulle accessible.
- Signalement clair des fichiers OneDrive ou cloud Windows encore disponibles uniquement en ligne, sans lancer silencieusement un long téléchargement pendant le lot.
- Distinction entre une annulation et un échec de conversion dans les résultats.

Cette version Windows est recommandée. Fermez la 0.3.1 et lancez `LocalAIReadyConverter-0.3.2-Setup.exe` ; aucune désinstallation préalable n’est nécessaire.

## 0.3.1 — première version Windows (23 septembre 2026)

- Interface organisée autour des fichiers à convertir et des résultats conservés entre lots.
- Assistant de découverte, filtre par type, sélection et formats ajustables par fichier.
- Nommage des sorties d'après l'original avec `-Converted`, sans écrasement.
- PDF recherchable par OCR sélectionnable comme sortie ; CSV Windows-1252 pris en charge en entrée.
- Vérification manuelle des mises à jour GitHub et téléchargement de l'installateur avec contrôle de taille et de SHA-256.
- Lien de soutien Stripe facultatif et libellés étoile GitHub/Stripe en français et anglais.
- Setup autonome Windows 11 x64 avec outils de conversion, OCR, notices et sources tierces intégrés. Testé hors ligne dans un Windows Sandbox propre : installation, conversions/OCR, démarrage de WebView2 et désinstallation.

Téléchargez `LocalAIReadyConverter-0.3.1-Setup.exe` dans les [Releases](../../releases) et vérifiez son empreinte dans [SHA256SUMS.txt](SHA256SUMS.txt). Ne désinstallez pas une ancienne version : fermez l'application et lancez le nouveau setup.
