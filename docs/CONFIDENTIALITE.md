# Confidentialité : ce qui reste local, ce qui peut utiliser Internet

[Read in English](CONFIDENTIALITE.en.md) · [Accueil](../README.fr.md)

**Vos documents sont convertis sur votre ordinateur.** L'application lit les sources choisies, écrit les sorties dans la destination que vous réglez et ne transmet pas le contenu de ces documents à une IA ni à un service de conversion. Aucun compte n'est nécessaire et aucune ligne de commande n'est demandée. Les originaux ne sont pas modifiés.

Cette affirmation concerne **la conversion**, pas chaque fonction du programme ou de Windows. Voici la distinction :

| Action | Réseau ? | Contenu de vos documents ? |
| --- | --- | --- |
| Convertir un PDF, classeur, CSV, DOCX ou une image avec les outils embarqués | Pas requis pour l'opération de conversion | Lu et écrit localement |
| Vérifier une mise à jour ou ouvrir une page GitHub | Oui, à votre demande | Non transmis par l'application |
| Afficher les informations publiques du profil GitHub dans « À propos » | Oui, à l'ouverture de cette vue, avec repli local hors ligne | Non transmis |
| Ajouter une langue OCR par téléchargement | Oui, seulement si vous le demandez | Non transmis |
| Cliquer sur un lien de soutien ou une annonce | Le navigateur ouvre un site externe | Aucun document envoyé par l'application ; le site ouvert a sa propre politique |

L'espace de soutien peut être masqué dans les Paramètres. Une annonce éventuelle est une image intégrée au paquet, pas une image chargée depuis un serveur à chaque affichage ; aucun script de régie n'est intégré aujourd'hui. Voir l'[explication du soutien](SOUTIEN.md).

**Important pour Windows :** la fenêtre utilise Microsoft Edge **WebView2 Fixed Version** intégré. Ce runtime a ses propres conditions et peut avoir des fonctions réseau ou de protection Microsoft indépendantes de la logique de conversion. Microsoft Defender SmartScreen y est inclus et collecte et transmet des informations sur l'utilisateur à Microsoft conformément à la [déclaration de confidentialité Microsoft](https://aka.ms/privacy) et au [livre blanc SmartScreen](https://learn.microsoft.com/en-us/microsoft-edge/privacy-whitepaper#smartscreen). Ce n'est pas un envoi volontaire de documents par le moteur de conversion. Voir aussi la [documentation de distribution WebView2](https://learn.microsoft.com/microsoft-edge/webview2/concepts/distribution).

Les **fichiers de sortie peuvent contenir les mêmes données sensibles** que leurs originaux, parfois sous une forme plus facile à lire ou à rechercher. Choisissez une destination appropriée, protégez vos sauvegardes et relisez les données importantes avant de les partager. Un document stocké dans un dossier synchronisé par OneDrive ou un service semblable reste soumis aux réglages de ce service ; l'application ne contrôle pas cette synchronisation.

Le paquet incorpore des composants sous licences distinctes ; leurs droits, notices et sources requises sont décrits dans [Composants tiers](COMPOSANTS_TIERS.md) et livrés avec l'installateur.
