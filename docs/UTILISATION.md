# Guide d'utilisation

## Convertir

Glissez des fichiers ou dossiers dans la zone d'importation, ou utilisez les boutons d'ajout. La colonne **Fichiers à convertir** montre les dossiers et les fichiers ; vous pouvez filtrer par type, cocher les fichiers à traiter et retirer une ligne de la liste sans supprimer l'original.

Choisissez les formats de sortie pour le lot. Les capsules de chaque fichier permettent d'ajuster ce choix individuellement ; les formats incompatibles sont grisés. Cliquez sur **Convertir** sous les deux colonnes. Les résultats restent visibles à droite entre deux conversions. Cliquez sur la capsule d'un résultat pour sélectionner le fichier correspondant dans l'Explorateur.

Relancer sans changement ne reconvertit pas les sorties déjà présentes dans la session. Ajouter un format ne crée que la sortie manquante. Si l'original ou la destination change, une nouvelle conversion peut être nécessaire. Un nom déjà présent est numéroté ; il n'est pas écrasé.

## Destination

Dans **Paramètres**, choisissez :

- un dossier `Conversion-AAAA-MM-JJ` près des sources ;
- le même dossier que chaque original ;
- un dossier de destination choisi.

Les originaux restent intacts. Vérifiez l'espace disponible et les droits d'écriture de la destination avant un lot important.

## OCR

L'OCR reconnaît le texte des images et des PDF scannés. Le PDF OCR produit un nouveau PDF recherchable ; il peut être choisi seul. Les langues de reconnaissance se règlent dans **Paramètres**. Les langues de base sont embarquées ; des modèles supplémentaires peuvent être importés ou téléchargés à la demande.

## Choisir une sortie pour une IA

Pour un PDF, TXT est souvent le plus léger ; JSON ajoute notamment la séparation par page. Pour un classeur Excel tabulaire, les CSV par feuille sont généralement plus compacts que le JSON détaillé. Ce dernier garde davantage de structure et les formules. Une formule ne peut avoir de valeur calculée que si cette valeur était enregistrée dans le classeur : l'application ne recalcule pas Excel.

La qualité du texte dépend de la source. Un PDF peut contenir une couche texte imparfaite ; l'OCR et l'extraction ne garantissent pas une transcription sans erreur. Contrôlez les données sensibles ou les chiffres importants avant de les réutiliser.
