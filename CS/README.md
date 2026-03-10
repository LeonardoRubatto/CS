# CoutSalarie.fr

Calculateur du coût réel d'un recrutement en France — charges patronales, réduction RGDU 2026, AGIRC-ARRCO, mutuelle, tickets restaurant.

🌐 **[coutsalarie.fr](https://coutsalarie.fr)**

## Stack

Site statique HTML/CSS/JS — déployé sur Cloudflare Pages.

## Structure

```
CS/
├── index.html            # Calculateur principal
├── confidentialite.html  # Politique de confidentialité
├── 404.html              # Page d'erreur
├── robots.txt
├── sitemap.xml
├── _redirects            # Redirections Cloudflare Pages
├── _headers              # Headers HTTP Cloudflare Pages
└── favicon.png           # À ajouter
```

## Déploiement Cloudflare Pages

1. Pousser ce repo sur GitHub
2. Dans Cloudflare Pages → **Create a project** → connecter le repo GitHub
3. Build settings : aucun (site statique)
   - Framework preset : `None`
   - Build command : *(laisser vide)*
   - Build output directory : `/` (ou `.`)
4. Déployer
5. **Important** : le site est dans le sous-dossier `CS/`.
     - Option A (recommandée) : **Root directory = `CS`**
     - Option B : garder la racine du repo, mais alors `Build output directory = CS`

## Fichiers images à ajouter

Avant le premier déploiement, ajouter à la racine :
- `favicon.png` (32×32 px)
- `apple-touch-icon.png` (180×180 px)
- `og-image.png` (1200×630 px) — utilisée pour les partages réseaux sociaux
