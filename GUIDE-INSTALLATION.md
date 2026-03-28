# 📱 Guide d'installation — BoutiquePOS Pro sur Android

## Option 1 : Installation directe PWA (Recommandé)
### Via Chrome sur votre téléphone Android

1. **Copiez le dossier BoutiquePOS-Pro** sur votre téléphone ou serveur local
2. Ouvrez Chrome sur Android et naviguez vers `index.html`
3. Appuyez sur le menu ⋮ (3 points) → **"Ajouter à l'écran d'accueil"**
4. L'application s'installe comme une vraie app Android
5. Elle fonctionne **hors ligne** grâce au Service Worker

---

## Option 2 : Générer un vrai APK (Gratuit)

### Méthode A — PWABuilder.com (Recommandé)
1. Hébergez les fichiers du dossier sur un serveur (ex: GitHub Pages, Netlify)
2. Allez sur **https://www.pwabuilder.com**
3. Entrez l'URL de votre app
4. Cliquez **"Package for stores"** → **Android**
5. Téléchargez l'APK signé

### Méthode B — Bubblewrap CLI (Local)
```bash
npm install -g @bubblewrap/cli
bubblewrap init --manifest https://votre-url/manifest.json
bubblewrap build
```

### Méthode C — Android Studio
1. Installez Android Studio
2. Créez un projet "Empty Activity"
3. Ajoutez WebView dans activity_main.xml
4. Copiez les fichiers dans assets/
5. Compilez et installez l'APK

---

## Option 3 : Serveur Local WiFi
Pour utiliser l'app sur plusieurs appareils sur votre réseau WiFi :

```bash
# Python
python3 -m http.server 8080 --directory BoutiquePOS-Pro/
```

Accédez depuis n'importe quel appareil : `http://[IP-de-votre-PC]:8080`

---

## Fonctionnalités
- Fonctionne hors ligne (Service Worker)
- Données sauvegardées localement
- Interface plein écran sur Android
- Optimisé pour écran tactile

## Configuration IA Photo
1. Créez un compte sur https://console.anthropic.com
2. Générez une clé API (sk-ant-...)
3. Dans l'app → Paramètres → Clé API Anthropic
