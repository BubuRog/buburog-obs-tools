# buburog_death_counter.html — Compteur de morts / Death Counter

---

## 🇫🇷 Français

### Description
Widget HTML pour OBS affichant le nombre de morts en Hardcore sous forme d'image animée.
Se connecte à **StreamElements** via un compteur nommé `deaths`.
L'image change à chaque mort avec un flash rouge animé.
Les images sont hébergées sur un dépôt GitHub séparé (`buburog-stream-assets`).

### Prérequis
- OBS Studio (toute version récente)
- Un compte **StreamElements** avec un compteur nommé `deaths`
- Un dépôt GitHub contenant les images `01.png` à `20.png`

### Configuration
Ouvre le fichier et modifie :

```javascript
const JWT_TOKEN      = "TON_JWT_TOKEN_ICI";   // StreamElements → Mon compte → Jetons d'accès
const CHANNEL_ID     = "TON_CHANNEL_ID_ICI";  // StreamElements → Mon compte → ID de chaîne
const IMAGE_BASE_URL = "URL_DE_TES_IMAGES/";  // URL raw GitHub de ton dossier d'images
```

### Format des images
Les images doivent être nommées `01.png`, `02.png`, ... `20.png` et hébergées en accès public.
URL raw GitHub : `https://raw.githubusercontent.com/TON_USER/TON_REPO/main/`

### Installation dans OBS
1. Ajoute une source → **Navigateur**
2. Coche **Fichier local** et sélectionne `buburog_death_counter.html`
3. Largeur : `200` / Hauteur : `200`
4. Positionne l'overlay sur ta scène

### Incrémenter le compteur
Dans StreamElements, incrémente le compteur `deaths` de +1 à chaque mort.
Tu peux lier ça à une commande chat `!death` via les bots StreamElements.

### Licence
MIT — libre d'utilisation, de modification et de redistribution.

---

## 🇬🇧 English

### Description
OBS HTML widget displaying the Hardcore death count as an animated image.
Connects to **StreamElements** via a counter named `deaths`.
The image changes on each death with a red flash animation.
Images are hosted on a separate GitHub repository (`buburog-stream-assets`).

### Requirements
- OBS Studio (any recent version)
- A **StreamElements** account with a counter named `deaths`
- A GitHub repository containing images `01.png` to `20.png`

### Configuration
Open the file and edit:

```javascript
const JWT_TOKEN      = "YOUR_JWT_TOKEN_HERE";   // StreamElements → My Account → Access Tokens
const CHANNEL_ID     = "YOUR_CHANNEL_ID_HERE";  // StreamElements → My Account → Channel ID
const IMAGE_BASE_URL = "YOUR_IMAGES_URL/";      // Raw GitHub URL of your images folder
```

### Image Format
Images must be named `01.png`, `02.png`, ... `20.png` and hosted publicly.
Raw GitHub URL: `https://raw.githubusercontent.com/YOUR_USER/YOUR_REPO/main/`

### OBS Installation
1. Add a source → **Browser**
2. Check **Local file** and select `buburog_death_counter.html`
3. Width: `200` / Height: `200`
4. Position the overlay on your scene

### Incrementing the Counter
In StreamElements, increment the `deaths` counter by +1 on each death.
You can link this to a chat command `!death` via StreamElements bots.

### License
MIT — free to use, modify and redistribute.
