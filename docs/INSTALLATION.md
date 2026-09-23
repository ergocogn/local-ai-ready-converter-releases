# Installer et mettre à jour sur Windows

[Read in English](INSTALLATION.en.md) · [Accueil](../README.fr.md)

## Installation

1. Utilisez Windows 11 x64.
2. Téléchargez le fichier `LocalAIReadyConverter-X.Y.Z-Setup.exe` depuis les [Releases](../../../releases).
3. Lancez le setup et suivez l'assistant. L'installation se fait pour votre compte Windows.
4. Ouvrez **Local AI-Ready Converter** depuis le menu Démarrer ou à la dernière étape du setup.

Ne téléchargez pas un fichier portant `.incomplete` ou `.part`. Les outils de conversion et les langues OCR de base sont inclus : pas besoin d'installer séparément Python, Pandoc ou Tesseract sur le poste utilisateur. L'application n'exige aucune ligne de commande.

## Mise à jour

Dans **Paramètres → Mises à jour**, lancez une vérification. Si une version plus récente est disponible, l'application peut télécharger le setup et le montrer dans l'Explorateur. Elle ne l'exécute pas et ne l'installe pas automatiquement.

Fermez l'application, puis lancez le nouveau setup. **Ne désinstallez pas la version précédente** : le setup la remplace. Vos documents ne sont pas gérés par l'installateur ; les paramètres utilisateur sont conservés.

Une vérification contre une vraie Release publique n'a pas encore été effectuée : le dépôt de distribution est toujours privé. Le code des mises à jour a été testé avec des réponses GitHub simulées.

## Désinstallation

Utilisez **Paramètres Windows → Applications installées → Local AI-Ready Converter → Désinstaller**. La désinstallation retire l'application, pas vos documents ni les fichiers convertis.

Si l'installation ou une mise à jour échoue, fermez toute fenêtre de l'application et réessayez. Pour signaler un problème, ouvrez une [Issue](../../../issues) en indiquant Windows, la version de l'application et le message d'erreur, sans joindre de document confidentiel.
