# Confidentialité et composants intégrés

Les documents sélectionnés sont lus et convertis sur l'ordinateur. L'application n'exige pas de compte et n'envoie pas le contenu de vos documents à une IA distante. Les fichiers de sortie sont écrits à la destination que vous choisissez.

Certaines actions **facultatives** utilisent le réseau : vérifier les Releases GitHub, afficher les informations publiques d'ergoCogn sur GitHub, ouvrir un lien d'aide ou de soutien, et télécharger un modèle OCR demandé par l'utilisateur. Une éventuelle annonce doit être configurée séparément ; aucune campagne n'est fournie par défaut.

L'interface Windows embarque **Microsoft Edge WebView2 Fixed Version**. Ce runtime possède ses propres conditions et peut avoir des fonctions réseau ou de protection Microsoft indépendantes de la conversion des documents. Son [mode de distribution](https://learn.microsoft.com/microsoft-edge/webview2/concepts/distribution) et les notices détaillées sont inclus dans le paquet.

**Notice Microsoft Defender SmartScreen :** le runtime WebView2 inclut SmartScreen. Cette fonction peut collecter et transmettre à Microsoft des informations relatives à l'utilisateur conformément à la [déclaration de confidentialité Microsoft](https://aka.ms/privacy) et au [livre blanc Microsoft Edge sur SmartScreen](https://learn.microsoft.com/en-us/microsoft-edge/privacy-whitepaper#smartscreen). Ce point concerne le runtime Microsoft, pas un envoi volontaire de vos documents au service de conversion.

Le paquet comporte aussi des composants libres sous licences distinctes, notamment Pandoc (GPL), OCRmyPDF et pikepdf (MPL), ainsi que fpdf2 et img2pdf (LGPL). La licence propriétaire de l'application ne retire aucun droit sur ces composants. Leurs textes et notices accompagnent l'installation dans `licenses/`. Voir [les composants tiers](COMPOSANTS_TIERS.md). Une revue finale des obligations de redistribution et de l'accès aux sources correspondantes est en cours avant toute Release publique.
