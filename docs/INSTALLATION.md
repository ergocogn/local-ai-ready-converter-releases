# Installer et mettre à jour

[Read in English](INSTALLATION.en.md) · [Accueil](../README.fr.md)

## Windows 11 x64

1. Téléchargez `LocalAIReadyConverter-X.Y.Z-Setup.exe` depuis les [Releases](../../../releases).
2. Lancez le setup et suivez l'assistant. L'installation se fait pour votre compte Windows.
3. Ouvrez **Local AI-Ready Converter** depuis le menu Démarrer ou à la dernière étape du setup.

Ne téléchargez pas un fichier portant `.incomplete` ou `.part`. Le setup contient les outils de conversion et les langues OCR de base : pas besoin d'installer séparément Python ou Tesseract. Aucune ligne de commande n'est nécessaire.

Pour une mise à jour, fermez l'application et lancez le nouveau setup. **Ne désinstallez pas l'ancienne version** : le setup la met à niveau. Les préférences sont conservées et l'installateur ne gère pas vos documents. Pour désinstaller, utilisez **Paramètres Windows → Applications installées → Local AI-Ready Converter → Désinstaller**.

## Linux x86_64

1. Téléchargez `LocalAIReadyConverter-X.Y.Z-Linux-x86_64.AppImage` depuis les [Releases](../../../releases).
2. Dans votre gestionnaire de fichiers, ouvrez **Propriétés → Permissions** et autorisez l'exécution du fichier comme un programme.
3. Double-cliquez sur l'AppImage.

L'AppImage est portable : elle ne nécessite aucune installation globale. Elle a été validée sur une VM Ubuntu Desktop 24.04 propre et contient Python, Tesseract, les langues OCR de base et un runtime AppImage statique moderne ; `libfuse2` n'est pas requis. Pour la retirer, supprimez l'AppImage. Vos originaux et fichiers convertis ne sont pas supprimés.

## Mises à jour

Dans **Paramètres → Mises à jour**, lancez une vérification. Si une Release plus récente contient un paquet natif compatible, l'application le télécharge, vérifie sa taille et son empreinte SHA-256, puis l'affiche dans le gestionnaire de fichiers. Elle ne l'exécute ni ne l'installe silencieusement.

Sous Windows, fermez l'application et lancez le setup téléchargé. Sous Linux, fermez l'application et ouvrez la nouvelle AppImage ; après un téléchargement vérifié, l'application lui attribue le droit d'exécution. L'installation d'une mise à jour reste une action manuelle et visible.

Si l'installation, le démarrage ou la mise à jour échoue, fermez toutes les fenêtres de l'application et réessayez. [Signalez le problème](../../../issues) avec votre système, la version de l'application et le message exact, sans jamais joindre de document confidentiel.
