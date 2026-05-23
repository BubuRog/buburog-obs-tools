# buburog_build.html — Afficheur de build actuel / Current Build Display

---

## 🇫🇷 Français

### Description
Widget HTML pour OBS affichant le build actuellement joué en overlay sur le stream.
Se connecte à **StreamElements** via un compteur pour changer de build à la volée sans quitter OBS.
Supporte 5 builds de Rogue Diablo 4 avec couleurs distinctes.

### Builds disponibles
| # | Code | Nom EN | Nom FR | Couleur |
|---|------|--------|--------|---------|
| 1 | PTB | Poison Twisting Blades | Lames sournoises empoisonnées | 🟢 Vert |
| 2 | DT  | Death Trap | Pièges mortels | 🟣 Violet |
| 3 | PS  | Penetrating Shot | Tir pénétrant | 🔵 Bleu |
| 4 | RF  | Rapid Fire | Tir rapide | 🩵 Cyan |
| 5 | ROA | Rain of Arrows | Pluie de Flèches | 🟠 Orange |

### Prérequis
- OBS Studio (toute version récente)
- Un compte **StreamElements** avec un compteur nommé `currentbuild`

### Configuration StreamElements
1. Va sur streamelements.com → **Mon compte** → **Jetons d'accès** → copie ton JWT
2. Note ton **ID de chaîne** (visible dans l'URL de ton dashboard)
3. Crée un compteur nommé `currentbuild` dans StreamElements

Ouvre le fichier et modifie :
```javascript
const JWT_TOKEN  = "TON_JWT_TOKEN_ICI";   // StreamElements → Mon compte → Jetons d'accès
const CHANNEL_ID = "TON_CHANNEL_ID_ICI";  // StreamElements → Mon compte → ID de chaîne
```

### Changer de build en cours de stream
Dans StreamElements, mets le compteur `currentbuild` à la valeur correspondante :
- `1` → Poison Twisting Blades
- `2` → Death Trap
- `3` → Penetrating Shot
- `4` → Rapid Fire
- `5` → Rain of Arrows

### Installation dans OBS
1. Ajoute une source → **Navigateur**
2. Coche **Fichier local** et sélectionne `buburog_build.html`
3. Largeur : `350` / Hauteur : `200`
4. Positionne l'overlay où tu le souhaites sur ta scène

### Licence
MIT — libre d'utilisation, de modification et de redistribution.

---

## 🇬🇧 English

### Description
OBS HTML widget displaying the currently played build as a stream overlay.
Connects to **StreamElements** via a counter to switch builds on the fly without leaving OBS.
Supports 5 Diablo 4 Rogue builds with distinct colors.

### Available Builds
| # | Code | Name EN | Name FR | Color |
|---|------|---------|---------|-------|
| 1 | PTB | Poison Twisting Blades | Lames sournoises empoisonnées | 🟢 Green |
| 2 | DT  | Death Trap | Pièges mortels | 🟣 Purple |
| 3 | PS  | Penetrating Shot | Tir pénétrant | 🔵 Blue |
| 4 | RF  | Rapid Fire | Tir rapide | 🩵 Cyan |
| 5 | ROA | Rain of Arrows | Pluie de Flèches | 🟠 Orange |

### Requirements
- OBS Studio (any recent version)
- A **StreamElements** account with a counter named `currentbuild`

### StreamElements Setup
1. Go to streamelements.com → **My Account** → **Access Tokens** → copy your JWT
2. Note your **Channel ID** (visible in your dashboard URL)
3. Create a counter named `currentbuild` in StreamElements

Open the file and edit:
```javascript
const JWT_TOKEN  = "YOUR_JWT_TOKEN_HERE";   // StreamElements → My Account → Access Tokens
const CHANNEL_ID = "YOUR_CHANNEL_ID_HERE";  // StreamElements → My Account → Channel ID
```

### Switching Builds During Stream
In StreamElements, set the `currentbuild` counter to the matching value:
- `1` → Poison Twisting Blades
- `2` → Death Trap
- `3` → Penetrating Shot
- `4` → Rapid Fire
- `5` → Rain of Arrows

### OBS Installation
1. Add a source → **Browser**
2. Check **Local file** and select `buburog_build.html`
3. Width: `350` / Height: `200`
4. Position the overlay wherever you want on your scene

### License
MIT — free to use, modify and redistribute.
