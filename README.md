# AccèsGrandMTL ♿

Répertoire web gratuit, multilingue (7 langues) et mis à jour automatiquement chaque semaine pour répertorier les lieux accessibles aux personnes à mobilité réduite dans le **Grand Montréal (Montréal, Rive-Sud et Rive-Nord/Laval)**.

## Contenu du dossier
- `index.html` : Le site web complet (carte interactive, filtres, 10 catégories, mode sombre, fiche imprimable pour patients, 7 langues).
- `data/curated_places.json` : Base clinique vérifiée (hôpitaux, centres de réadaptation, aides techniques, piscines adaptées, REM/STM, musées Kéroul, etc.).
- `data/custom_places.csv` : Tableau simple où vous ou vos collègues pouvez ajouter des cliniques, restaurants ou services sans coder.
- `data/places.json` : Base complète chargée par le site (générée automatiquement avec 800 à 2 500+ lieux réels).
- `scripts/update_places.py` : Robot Python qui interroge OpenStreetMap par secteur (Montréal, Rive-Sud, Rive-Nord), nettoie les doublons et fusionne les sources.
- `.github/workflows/weekly-update.yml` : Automatisation GitHub Actions (mise à jour chaque dimanche à 3 h + bouton manuel en 1 clic).

## Mise en ligne en 5 minutes (sans coder)

1. Créez un dépôt public sur GitHub (ex. `acces-grand-mtl`).
2. Décompressez le fichier ZIP sur votre ordinateur, puis glissez **tous les fichiers et dossiers** (y compris le dossier caché `.github`) dans votre dépôt GitHub (ou utilisez **Add file → Upload files**).
   - *Note : Si votre ordinateur cache le dossier `.github`, créez simplement le fichier manuellement dans GitHub via **Add file → Create new file**, tapez exactement `.github/workflows/weekly-update.yml` comme nom et collez son contenu.*
3. Activez le lien web public : allez dans **Settings → Pages**, choisissez `Deploy from a branch`, sélectionnez `main` et `/ (root)`, puis cliquez sur **Save**.
4. Importez immédiatement vos 800 à 2 500+ lieux réels : allez dans l'onglet **Actions** de votre dépôt → cliquez sur **Mise à jour hebdomadaire des lieux accessibles** → cliquez sur **Run workflow** → bouton vert **Run workflow**.
5. Attendez environ 60 à 90 secondes : le fichier `data/places.json` sera mis à jour automatiquement, puis se réactualisera tout seul **chaque dimanche matin** !
