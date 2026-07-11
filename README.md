# Portfolio Henri Linke — site une page (FR + EN)

Site statique autonome (`index.html` + miroir anglais `en/index.html`, aucun build, aucune dépendance à installer).
Positionnement : **portfolio d'ingénieur IA** à double lecture — recruteurs CDI en priorité, clients potentiels en second plan discret.
Conçu pour être publié gratuitement.

## ✅ À VÉRIFIER avant de publier
- [x] **Email confirmé** : `linke.henri@proton.me` (adresse pro, intégrée dans Contact).
- [x] Téléphone + LinkedIn vérifiés dans la section Contact (`index.html`).
- [x] Relire les 5 études de cas (KerAwen live + stock + NF525 + multi-agents + dev assisté par IA ; textes 100% vrais).
- [ ] Tenir `assets/CV_Henri_Linke_FR.pdf` / `_EN.pdf` synchronisés avec le CV de référence (projet « recherche emploi Henri », `commun/cv-final/`).
- [ ] Toute modification de contenu doit être répercutée dans les deux langues (`index.html` **et** `en/index.html`).

## 📸 Captures & assets
- `assets/kerawen-search.webp`, `kerawen-ai.webp` : captures du projet public **support.kerawen.com** (portail doc + recherche + assistant IA). Le SVG d'architecture est inline dans l'HTML. **Toujours pousser le dossier `assets/` complet avec `index.html`**.
- `assets/stock-dashboard.webp` + `stock-rapports.webp` : captures du cas d'automatisation de workflows multi-magasins (SaaS stock, projet privé, données floutées).
- `assets/og-cover.png` / `og-cover-en.png` (1200×630) : images d'aperçu de partage de lien (Open Graph + Twitter card), référencées dans les `<meta>` de chaque page. Régénérables en HTML → capture headless 1200×630.
- `assets/CV_Henri_Linke_FR.pdf` / `_EN.pdf` : CV téléchargeables (boutons héro + contact), copies du CV de référence.
- Captures servies en **WebP** (≈ 57 % plus légères que les PNG d'origine ; les PNG sources ne sont plus dans le dépôt — re-capturer depuis les sites si besoin).
- Les cas multi-agents, NF525 et dev assisté par IA sont purement textuels.
- 1 étude de cas pointe vers le live (support.kerawen.com) avec badge « En ligne ».
- Les captures s'intègrent toutes dans le format `figure.media`.

## Option A — GitHub Pages (recommandé, gratuit)
1. Crée un dépôt GitHub **public**, ex. `portfolio` (ou `lnkhenri.github.io` pour l'avoir à la racine).
2. Pousse le contenu de ce dossier (`index.html` + `README.md`) à la racine du dépôt :
   ```bash
   cd portfolio
   git init && git add . && git commit -m "Portfolio"
   git branch -M main
   git remote add origin git@github.com:lnkhenri/portfolio.git
   git push -u origin main
   ```
3. GitHub → dépôt → **Settings → Pages** → *Source : Deploy from a branch* → branche `main`, dossier `/ (root)` → Save.
4. Ton site est en ligne sous ~1 min à :
   - `https://lnkhenri.github.io/portfolio/`  (dépôt `portfolio`)
   - `https://lnkhenri.github.io/`  (dépôt `lnkhenri.github.io`)

## Option B — Netlify / Cloudflare Pages (glisser-déposer, encore plus simple)
- **Netlify** : https://app.netlify.com/drop → glisse le dossier `portfolio/` → URL en ligne immédiate.
- **Cloudflare Pages** : créer un projet → connecter le dépôt GitHub → build command vide, output `/`.

### En-têtes HTTP (`_headers`)
Le fichier `_headers` pose des en-têtes de **sécurité** (CSP, HSTS, `X-Content-Type-Options`, `Referrer-Policy`, `Permissions-Policy`) et un **cache long** sur `/assets/*`. Il est lu automatiquement par **Netlify** et **Cloudflare Pages**. **GitHub Pages l'ignore** (il ne sait pas poser d'en-têtes custom) — c'est l'une des raisons de préférer Netlify/Cloudflare. Le fichier `.nojekyll` évite tout traitement Jekyll côté GitHub Pages.

## Domaine personnalisé (optionnel, ~10-12 €/an)
Un domaine type `henri-linke.fr` ou `henrilinke.dev` fait beaucoup plus pro qu'une URL `github.io`.
GitHub Pages, Netlify et Cloudflare permettent tous de brancher un domaine perso gratuitement
(tu paies seulement le nom de domaine). À faire une fois le site validé.

> ⚠️ **Une fois l'URL fixée** : dans `index.html`, ajouter `<link rel="canonical">` + `<meta property="og:url">`, et passer `og:image` / `twitter:image` en URL **absolue** (`https://ton-domaine/assets/og-cover.png`) pour un aperçu de lien fiable sur toutes les plateformes. Un commentaire le rappelle déjà dans le `<head>`.

## Modifier le site
Tout est dans `index.html` (HTML + CSS + un peu de JS, dans un seul fichier), avec un miroir anglais dans `en/index.html` à maintenir en parallèle. Édite, commit, push : GitHub Pages redéploie automatiquement.
