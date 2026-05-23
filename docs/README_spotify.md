# buburog_spotify.html — Now Playing Spotify

---

## 🇫🇷 Français

### Description
Widget HTML pour OBS affichant la musique Spotify en cours de lecture en temps réel.
Affiche : pochette d'album, titre, artiste, barre de progression et temps.
Se connecte directement à l'**API Spotify** via OAuth.

### Prérequis
- Un compte **Spotify** (gratuit ou Premium)
- Une application créée sur [developer.spotify.com](https://developer.spotify.com)

### Configuration — Étape par étape

#### 1. Créer une application Spotify
1. Va sur [developer.spotify.com/dashboard](https://developer.spotify.com/dashboard)
2. Clique **"Create app"**
3. Nom : ce que tu veux (ex: `BubuRog OBS`)
4. Redirect URI : `http://localhost:8888/callback`
5. Coche **"Web API"**
6. Récupère ton **Client ID** et **Client Secret**

#### 2. Générer le Refresh Token
C'est l'étape la plus technique. Ouvre cette URL dans ton navigateur en remplaçant `TON_CLIENT_ID` :
```
https://accounts.spotify.com/authorize?client_id=TON_CLIENT_ID&response_type=code&redirect_uri=http://localhost:8888/callback&scope=user-read-currently-playing
```
Autorise l'accès → récupère le `code` dans l'URL de redirection, puis échange-le contre un Refresh Token via l'API Spotify. Consulte la [documentation Spotify](https://developer.spotify.com/documentation/web-api/tutorials/code-flow) pour le détail.

#### 3. Remplir les variables
```javascript
const CLIENT_ID     = "TON_CLIENT_ID_ICI";      // developer.spotify.com → Dashboard → Client ID
const CLIENT_SECRET = "TON_CLIENT_SECRET_ICI";  // developer.spotify.com → Dashboard → Client Secret
const REFRESH_TOKEN = "TON_REFRESH_TOKEN_ICI";  // Généré à l'étape 2
```

### ⚠️ Sécurité
Ne partage **jamais** ton Client Secret ni ton Refresh Token publiquement.
Si tu les exposes accidentellement, régénère-les immédiatement sur le dashboard Spotify.

### Installation dans OBS
1. Ajoute une source → **Navigateur**
2. Coche **Fichier local** et sélectionne `buburog_spotify.html`
3. Largeur : `550` / Hauteur : `200`
4. Positionne l'overlay sur ta scène

### Licence
MIT — libre d'utilisation, de modification et de redistribution.

---

## 🇬🇧 English

### Description
OBS HTML widget displaying the currently playing Spotify track in real time.
Shows: album art, title, artist, progress bar and timestamps.
Connects directly to the **Spotify API** via OAuth.

### Requirements
- A **Spotify** account (free or Premium)
- An app created on [developer.spotify.com](https://developer.spotify.com)

### Configuration — Step by Step

#### 1. Create a Spotify App
1. Go to [developer.spotify.com/dashboard](https://developer.spotify.com/dashboard)
2. Click **"Create app"**
3. Name: anything you want (e.g. `BubuRog OBS`)
4. Redirect URI: `http://localhost:8888/callback`
5. Check **"Web API"**
6. Grab your **Client ID** and **Client Secret**

#### 2. Generate the Refresh Token
Open this URL in your browser, replacing `YOUR_CLIENT_ID`:
```
https://accounts.spotify.com/authorize?client_id=YOUR_CLIENT_ID&response_type=code&redirect_uri=http://localhost:8888/callback&scope=user-read-currently-playing
```
Authorize access → grab the `code` from the redirect URL, then exchange it for a Refresh Token via the Spotify API. See [Spotify docs](https://developer.spotify.com/documentation/web-api/tutorials/code-flow) for details.

#### 3. Fill in the Variables
```javascript
const CLIENT_ID     = "YOUR_CLIENT_ID_HERE";     // developer.spotify.com → Dashboard → Client ID
const CLIENT_SECRET = "YOUR_CLIENT_SECRET_HERE"; // developer.spotify.com → Dashboard → Client Secret
const REFRESH_TOKEN = "YOUR_REFRESH_TOKEN_HERE"; // Generated in step 2
```

### ⚠️ Security Warning
**Never** share your Client Secret or Refresh Token publicly.
If accidentally exposed, regenerate them immediately on the Spotify dashboard.

### OBS Installation
1. Add a source → **Browser**
2. Check **Local file** and select `buburog_spotify.html`
3. Width: `550` / Height: `200`
4. Position the overlay on your scene

### License
MIT — free to use, modify and redistribute.
