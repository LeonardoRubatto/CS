# CoutSalarie.fr

**Domaine :** coutsalarie.fr  
**Langue :** fr  
**Catégorie :** finance  
**Couleur accent :** `#1D4ED8` (blue)

## Fonctionnalités clés

- Calcul du coût total employeur à partir du salaire net ou brut
- Réduction RGDU 2026 (LFSS 2025 art. 18) — seuil élargi à 3 SMIC, coefficient dégressif exact
- Options compléments : mutuelle collective, tickets restaurant, transport, versement mobilité, médecine du travail
- Statut cadre/non-cadre, effectif, région (France métro / Alsace-Moselle / DOM-TOM), secteur AT/MP
- Breakdown complet cadre par cadre (charges salariales + patronales + compléments + réduction RGDU)
- Export PDF, partage par URL avec état encodé
- Dark mode avec anti-flash et icônes SVG locales
- Portal bridge `window.__CALC_STATE__`

## Structure des fichiers

```
CS/
├── index.html
├── confidentialite.html
├── 404.html
├── robots.txt
├── sitemap.xml
├── readme.md
├── _headers
├── assets/
│   └── icons/
│       ├── warning.svg
│       ├── info.svg
│       ├── error.svg
│       ├── success.svg
│       ├── share.svg
│       ├── pdf.svg
│       ├── sources.svg
│       ├── theme-dark.svg
│       ├── theme-light.svg
│       ├── france.svg
│       └── [icônes domaine complémentaires]
├── favicon.png          (32×32)
├── apple-touch-icon.png (180×180)
└── og-image.png         (1200×630)
```

## Icônes

Installer les fichiers SVG dans `/assets/icons/`.  
Icônes canoniques requises : `warning.svg`, `info.svg`, `error.svg`, `success.svg`, `share.svg`, `pdf.svg`, `sources.svg`, `theme-dark.svg`, `theme-light.svg`, `france.svg`

## Sources des données

| Source | Vérification |
|--------|-------------|
| URSSAF — Taux de cotisations 2026 | 01/01/2026 |
| LFSS 2025 art. 18 — Réforme RGDU (Légifrance) | 01/01/2026 |
| AGIRC-ARRCO — Accord du 01/11/2023 | 01/01/2023 |
| Convention Unédic 2024 | 01/01/2024 |
| Décret n°2025-1446 — Vieillesse déplafonnée | 01/01/2026 |
| Service-Public.fr — Cotisations employeur | 01/01/2026 |

## Déploiement

Push sur GitHub → Cloudflare Pages détecte le commit et déploie automatiquement.  
Aucun outil de build requis — site statique pur HTML/CSS/JS.

## Mise à jour des données

Fréquence recommandée : **annuelle** (voire semestrielle — certains taux URSSAF changent en juillet).  
Prochaine vérification recommandée : **01/01/2027** — vérifier URSSAF, Unédic, AGIRC-ARRCO et Légifrance pour LFSS suivante.

## Assets graphiques

| Fichier | Dimensions | Contenu |
|---------|-----------|---------|
| `favicon.png` | 32×32 px | Fond `#1D4ED8`, lettres **C€** en blanc, bold, centré |
| `apple-touch-icon.png` | 180×180 px | Même design que favicon — iOS ajoute automatiquement les coins arrondis |
| `og-image.png` | 1200×630 px | Fond `#dde6ef`, card blanche centrée avec logo + « CoutSalarie.fr » + « Calcul du coût réel d'un salarié 2026 » |
