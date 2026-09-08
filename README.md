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

## Déploiement — GitHub Pages

Le site est publié depuis ce dépôt, branche `main`, dossier `/` (racine).

- URL : **https://lnkhenri.github.io/portfolio/**
- Version anglaise : **https://lnkhenri.github.io/portfolio/en/**

Sur un compte GitHub **gratuit**, Pages ne fonctionne que si le dépôt est **public**. Le passer en privé coupe le site (le plan Pro permet Pages sur un dépôt privé).

Le fichier `.nojekyll` est là pour que GitHub Pages serve les fichiers tels quels, sans passer par Jekyll.

## Domaine personnalisé (optionnel, ~10-12 €/an)

Un domaine type `henri-linke.fr` ou `henrilinke.dev` se branche sur GitHub Pages (Settings → Pages → Custom domain). Une fois l’URL changée, mettre à jour `canonical`, `og:url` et les URLs absolues `og:image` / `twitter:image` dans `index.html` et `en/index.html`.

## Modifier le site

Tout est dans `index.html` (HTML + CSS + un peu de JS), avec un miroir anglais dans `en/index.html` à tenir à jour en parallèle. Édite, commit, push : GitHub Pages redéploie tout seul.
