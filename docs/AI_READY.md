# Save tokens. Save energy. Use AI cleverly.

[Read in English](AI_READY.en.md) · [Accueil](../README.fr.md)

## L'idée en une phrase

Préparer une fois un document, puis réutiliser **la bonne information dans le bon format**, plutôt que remettre sans cesse le fichier brut entier dans une chaîne d'outils.

Un PDF scanné peut être une image sans texte sélectionnable. Un classeur peut contenir plusieurs feuilles, formules et cellules vides. Un document Word peut mêler titres, tableaux et paragraphes. Avant qu'une IA ou un moteur de recherche puisse exploiter ces contenus, quelqu'un doit souvent en extraire une représentation plus simple. Local AI-Ready Converter effectue cette **étape de préparation sur votre ordinateur** ; il ne choisit pas une IA à votre place.

## « Save tokens » : moins de contexte inutile, pas de magie

Un *token* est une unité traitée par un modèle de langage. Le coût, la vitesse et la place disponible dans son contexte dépendent en partie du nombre de tokens qu'on lui fournit. **Le cas du PDF envoyé directement à une API est concret :** [l'API d'OpenAI peut intégrer à son entrée le texte extrait et les images des pages](https://developers.openai.com/api/docs/guides/file-inputs). Si vous voulez seulement rechercher un montant ou résumer le texte, extraire localement le TXT puis n'envoyer que le passage utile peut réduire nettement le contexte et son coût. Ce n'est pas équivalent lorsque l'IA doit voir la mise en page, une image ou un graphique.

Pour un tableur, le CSV d'une seule feuille peut être bien plus compact qu'un JSON détaillant chaque cellule vide. À l'inverse, le JSON est utile si vous devez garder les pages d'un PDF, les formules ou une structure précise.

**Exemple concret :** convertissez un classeur en CSV et JSON. Pour demander à un agent « quelles lignes correspondent au produit X ? », transmettez seulement la feuille CSV concernée. Pour auditer une formule, reprenez le JSON. Vous choisissez la représentation en fonction de la question — il n'y a pas de format « IA » universel.

La conversion seule ne réduit pas automatiquement les tokens. Si vous envoyez **toutes** les sorties à un modèle, vous pouvez au contraire en utiliser davantage. L'application actuelle ne calcule pas les tokens économisés et ne décide pas encore quels passages transmettre.

## « Save energy » : éviter le travail répété, sans promesse chiffrée

L'OCR, l'analyse de documents et les appels à une IA consomment des ressources. Conserver un résultat TXT, Markdown, JSON ou CSV réutilisable peut éviter de refaire la même extraction à chaque demande. Traiter un lot localement permet aussi de préparer plusieurs fichiers dans un seul parcours. Mais l'ordinateur consomme lui-même de l'énergie pendant la conversion, et le gain total dépend de l'usage ultérieur. **Nous n'affirmons pas une économie d'énergie mesurée pour chaque fichier.** La devise exprime un objectif de conception : ne pas répéter inutilement des traitements.

## « Use AI cleverly » : garder le choix et la provenance

Une sortie préparée peut être relue **avant** de la transmettre à un agent. Vous pouvez ne partager qu'un extrait, choisir TXT pour la lecture, JSON pour les pages, CSV pour les tableaux, ou conserver les fichiers localement sans jamais utiliser d'IA. Les originaux restent intacts ; les nouveaux fichiers sont sous votre contrôle. Les conversions OCR et PDF ne garantissent pas l'exactitude : vérifiez notamment les montants, noms et tableaux importants.

La conversion documentaire est locale, mais certaines fonctions facultatives utilisent le réseau et le runtime Windows a ses propres comportements. La [page confidentialité](CONFIDENTIALITE.md) distingue ces aspects ; « local » ne signifie pas « aucune connexion possible ».

## Ce qui existe — et ce qui vient après

Aujourd'hui : import visuel, conversion locale, OCR, sorties ouvertes, sélection des formats et destinations. **Pas** de base vectorielle, recherche sémantique, API/MCP ni RAG intégrés.

La suite envisagée est progressive : un dossier AI-ready stable et un manifest JSON documentant les fichiers déjà produits ; un accès local API/MCP explicite pour éviter de refaire OCR et extraction ; puis découpage en passages, embeddings et index locaux ; enfin recherche sémantique et RAG local avec citations des passages. Chaque étape devra respecter le contrôle des documents et être testée séparément. Voir la [feuille de route](ROADMAP.md) et l'[architecture](ARCHITECTURE.md).
