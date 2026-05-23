# end.html — Scène de fin / End Scene

---

## 🇫🇷 Français

### Description
Widget HTML pour OBS à utiliser dans la scène **End** (écran de fin de stream).
Affiche une vidéo YouTube en plein cadre avec un cadre gothique décoratif.
**À la fin de la vidéo, OBS arrête automatiquement le stream.**

### Prérequis
- OBS Studio 28 ou supérieur
- Plugin WebSocket OBS activé (`Outils → Paramètres du serveur WebSocket`)

### Configuration
Ouvre le fichier et modifie les variables en haut du script :

```javascript
const OBS_HOST     = "127.0.0.1";            // Laisse tel quel si OBS est sur le même PC
const OBS_PORT     = 4455;                    // Port WebSocket OBS (défaut : 4455)
const OBS_PASSWORD = "TON_MOT_DE_PASSE_ICI"; // Outils → Paramètres WebSocket → Mot de passe
```

Remplace également l'ID de la vidéo YouTube si besoin :
```javascript
videoId: 'h1zk8rQYskY',  // Remplace par l'ID de ta vidéo YouTube de fin
```

### Installation dans OBS
1. Dans OBS, sélectionne ta scène **End**
2. Ajoute une source → **Navigateur**
3. Coche **Fichier local** et sélectionne `end.html`
4. Largeur : `520` / Hauteur : `340`
5. Coche **Actualiser le navigateur quand la scène devient active**

### ⚠️ Attention
Ce widget **arrête le stream définitivement** à la fin de la vidéo.
Ne l'utilise que dans ta scène de fin. Teste d'abord hors stream !

### Licence
MIT — libre d'utilisation, de modification et de redistribution.

---

## 🇬🇧 English

### Description
HTML widget for OBS to use in the **End** scene (end of stream screen).
Displays a YouTube video in a decorative gothic frame.
**When the video ends, OBS automatically stops the stream.**

### Requirements
- OBS Studio 28 or higher
- OBS WebSocket plugin enabled (`Tools → WebSocket Server Settings`)

### Configuration
Open the file and edit the variables at the top of the script:

```javascript
const OBS_HOST     = "127.0.0.1";            // Leave as-is if OBS runs on the same PC
const OBS_PORT     = 4455;                    // OBS WebSocket port (default: 4455)
const OBS_PASSWORD = "YOUR_PASSWORD_HERE";    // Tools → WebSocket Settings → Password
```

Also replace the YouTube video ID if needed:
```javascript
videoId: 'h1zk8rQYskY',  // Replace with your YouTube end video ID
```

### OBS Installation
1. In OBS, select your **End** scene
2. Add source → **Browser**
3. Check **Local file** and select `end.html`
4. Width: `520` / Height: `340`
5. Check **Refresh browser when scene becomes active**

### ⚠️ Warning
This widget **permanently stops the stream** when the video ends.
Only use it in your end scene. Test it outside of a live stream first!

### License
MIT — free to use, modify and redistribute.
