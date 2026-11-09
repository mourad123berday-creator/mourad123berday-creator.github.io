# Mettre le site Wa9tou en ligne (GitHub Pages, gratuit)

## 1. Créer le dépôt
1. Crée un compte sur https://github.com (si besoin).
2. « New repository » → nom EXACT : `<ton-pseudo>.github.io`
   (ex. `mouradberday.github.io`) → Public → Create.
   ⚠️ Ce nom donne un site à la RACINE du domaine, indispensable pour app-ads.txt.

## 2. Envoyer les fichiers
**Par le navigateur :** « Add file » → « Upload files » → glisse tous les
fichiers de ce dossier (index.html, ar.html, privacy.html, style.css,
app-ads.txt, .nojekyll) → « Commit changes ».

**Ou en ligne de commande :**
```bash
cd site
git init && git add . && git commit -m "Site Wa9tou"
git branch -M main
git remote add origin https://github.com/<ton-pseudo>/<ton-pseudo>.github.io.git
git push -u origin main
```

## 3. Activer GitHub Pages
Settings → Pages → Source : « Deploy from a branch » → Branch : `main` / `(root)` → Save.
Après 1–2 min, le site est en ligne :
- Accueil : `https://<ton-pseudo>.github.io/`
- Confidentialité : `https://<ton-pseudo>.github.io/privacy.html`
- AdMob : `https://<ton-pseudo>.github.io/app-ads.txt`

## 4. Renseigner les URL
- **Play Console → Compte de développeur → Détails du compte → Site Web** :
  `https://<ton-pseudo>.github.io/` (décocher « Je n'ai pas de site Web »).
- **Play Console → ton appli → Contenu de l'appli → Règles de confidentialité** :
  `https://<ton-pseudo>.github.io/privacy.html`
- **AdMob** : remplace `pub-XXXXXXXXXXXXXXXX` dans `app-ads.txt` par ton ID éditeur,
  re-commit, puis dans AdMob → Applis → app-ads.txt → « Vérifier ».

## 5. Quand l'appli est publiée
Dans `index.html` et `ar.html`, remplace `href="#"` du bouton par :
`https://play.google.com/store/apps/details?id=ma.wa9tou.app`
