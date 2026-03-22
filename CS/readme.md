# Calculateur Coût Salarié

> Calculateur de charges patronales et coût réel d'un recrutement — barèmes URSSAF 2026  
> Domaine : https://salaire.wecalc.fr · Langue : fr · Catégorie : Finance · Accent : `#1D4ED8`

## Fonctionnalités

- Calcul du coût employeur total à partir d'un salaire brut : cotisations patronales URSSAF 2026 détaillées ligne par ligne (maladie, retraite, chômage, accidents du travail, formation, etc.)
- Calcul inverse : estimation du salaire brut atteignable pour un budget employeur donné
- Décomposition complète : salaire brut → cotisations salariales → salaire net → coût total employeur
- Prise en compte des cas particuliers : statut cadre / non-cadre, secteurs d'activité, taux AT/MP configurables
- Partage de résultat par URL encodée, export PDF, dark mode, cookie banner RGPD, responsive mobile
- 4 blocs JSON-LD : `WebApplication`, `WebSite`, `BreadcrumbList`, `FAQPage` — rich results Google activés

## Structure des fichiers

```
CS/
├── index.html
├── confidentialite.html
├── 404.html
├── _headers
├── robots.txt
├── sitemap.xml
├── readme.md
├── favicon.png
├── apple-touch-icon.png
├── og-image.png
└── assets/
    └── icons/
        ├── logo-fibo4.svg
        ├── arrow.svg
        ├── bank.svg
        ├── bonus.svg
        ├── brief.svg
        ├── calc.svg
        ├── card.svg
        ├── cube.svg
        ├── egal.svg
        ├── error.svg
        ├── europe.svg
        ├── exam.svg
        ├── france.svg
        ├── info.svg
        ├── op.svg
        ├── pdf.svg
        ├── receipt-duotone.svg
        ├── share.svg
        ├── sources.svg
        ├── sources-dark.svg
        ├── student.svg
        ├── success.svg
        ├── theme-dark.svg
        ├── theme-light.svg
        ├── wallet-duotone.svg
        └── warning.svg
```

## Icônes SVG requises

Installer dans `/assets/icons/` : `logo-fibo4.svg`, `arrow.svg`, `bank.svg`, `bonus.svg`, `brief.svg`, `calc.svg`, `card.svg`, `cube.svg`, `egal.svg`, `error.svg`, `europe.svg`, `exam.svg`, `france.svg`, `info.svg`, `op.svg`, `pdf.svg`, `receipt-duotone.svg`, `share.svg`, `sources.svg`, `sources-dark.svg`, `student.svg`, `success.svg`, `theme-dark.svg`, `theme-light.svg`, `wallet-duotone.svg`, `warning.svg`

## Sources des données

| Source | Organisme | URL | Vérifié le |
|--------|-----------|-----|------------|
| Taux de cotisations patronales et salariales 2026 | URSSAF | https://www.urssaf.fr/accueil/employeur/calcul-des-cotisations.html | 2026-03-21 |
| Plafond annuel de la Sécurité Sociale (PASS) 2026 | URSSAF / Sécurité Sociale | https://www.urssaf.fr | 2026-03-21 |
| Taux de cotisation chômage (AGS, APEC) | France Travail / AGIRC-ARRCO | https://www.francetravail.fr | 2026-03-21 |
| Taux retraite complémentaire cadres / non-cadres | AGIRC-ARRCO | https://www.agirc-arrco.fr | 2026-03-21 |
| Contribution patronale formation professionnelle | OPCO | https://travail-emploi.gouv.fr | 2026-03-21 |

## Déploiement

Push GitHub → Cloudflare Pages. Aucun outil de build. Le dossier `CS/` est la racine du site.

```bash
git add .
git commit -m "update: [description courte]"
git push origin main
```

Cloudflare Pages détecte le push et redéploie automatiquement en ~30 secondes.

## Mise à jour des données

- Fréquence recommandée : annuelle — vérifier en janvier (nouveaux barèmes URSSAF et PASS)
- Prochaine vérification : janvier 2027
- Fichiers à mettre à jour : `index.html` (constantes dans `CFG` : taux, PASS, plafonds), `sitemap.xml` (`lastmod`)

## Assets graphiques à produire manuellement

| Fichier | Dimensions | Contenu |
|---------|------------|---------|
| `favicon.png` | 32×32 px | Fond `#1D4ED8`, lettres **C€** en blanc, bold, centré |
| `apple-touch-icon.png` | 180×180 px | Même design — iOS arrondit automatiquement les coins |
| `og-image.png` | 1200×630 px | Fond `#dde6ef`, card blanche centrée : logo + "Calculateur Charges Patronales 2026 — Coût Réel d'un Salarié" |

