# video_intro.html — Scène de démarrage / Start Scene

---

## 🇫🇷 Français

### Description
Widget HTML pour OBS à utiliser dans la scène **Start** (écran "Le stream commence bientôt").
Affiche une vidéo YouTube en plein cadre avec un cadre gothique décoratif.
**À la fin de la vidéo, OBS bascule automatiquement vers la scène Live.**

### Prérequis
- OBS Studio 28 ou supérieur
- Plugin WebSocket OBS activé (`Outils → Paramètres du serveur WebSocket`)

### Configuration
Ouvre le fichier et modifie les variables en haut du script :

```javascript
const OBS_HOST     = "127.0.0.1";          // Laisse tel quel si OBS est sur le même PC
const OBS_PORT     = 4455;                  // Port WebSocket OBS (défaut : 4455)
const OBS_PASSWORD = "TON_MOT_DE_PASSE_ICI"; // Outils → Paramètres WebSocket → Mot de passe
const TARGET_SCENE = "LIVE - GAMEPLAY";     // Nom exact de ta scène Live dans OBS
```

Remplace également l'ID de la vidéo YouTube si besoin :
```javascript
videoId: 'kwIEq7yUxwQ',  // Remplace par l'ID de ta vidéo YouTube
```

### Installation dans OBS
1. Dans OBS, sélectionne ta scène **Start**
2. Ajoute une source → **Navigateur**
3. Coche **Fichier local** et sélectionne `video_intro.html`
4. Largeur : `520` / Hauteur : `340`
5. Coche **Actualiser le navigateur quand la scène devient active**

### Licence
MIT — libre d'utilisation, de modification et de redistribution.

---

## 🇬🇧 English

### Description
HTML widget for OBS to use in the **Start** scene ("Stream starting soon" screen).
Displays a YouTube video in a decorative gothic frame.
**When the video ends, OBS automatically switches to the Live scene.**

### Requirements
- OBS Studio 28 or higher
- OBS WebSocket plugin enabled (`Tools → WebSocket Server Settings`)

### Configuration
Open the file and edit the variables at the top of the script:

```javascript
const OBS_HOST     = "127.0.0.1";            // Leave as-is if OBS runs on the same PC
const OBS_PORT     = 4455;                    // OBS WebSocket port (default: 4455)
const OBS_PASSWORD = "YOUR_PASSWORD_HERE";    // Tools → WebSocket Settings → Password
const TARGET_SCENE = "LIVE - GAMEPLAY";       // Exact name of your Live scene in OBS
```

Also replace the YouTube video ID if needed:
```javascript
videoId: 'kwIEq7yUxwQ',  // Replace with your YouTube video ID
```

### OBS Installation
1. In OBS, select your **Start** scene
2. Add source → **Browser**
3. Check **Local file** and select `video_intro.html`
4. Width: `520` / Height: `340`
5. Check **Refresh browser when scene becomes active**

### License
MIT — free to use, modify and redistribute.
