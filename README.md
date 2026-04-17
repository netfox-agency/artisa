# Maison Artisa

Site e-commerce headless pour [Maison Artisa](https://artisacosmetique.com) — cosmétiques naturels fabriqués sur commande.

## Stack

- **Frontend** : HTML + CSS + JavaScript vanilla (pas de framework, pas de build)
- **Commerce** : Shopify Storefront API (headless)
- **Hébergement** : Vercel
- **Domaine** : artisacosmetique.com

## Structure

- `index.html` — Landing page
- `product.html` — Fiche produit (lit `?h=<handle>` pour fetch Shopify)
- `reviews.html` — Page avis clients
- `*.jpg` / `*.webp` — Assets images optimisés

## Déploiement

Auto-deploy via Vercel sur chaque push vers `main`.

## Backend Shopify

- Store : `artisa-8569.myshopify.com` (domaine primaire utilisé pour le checkout)
- Storefront API version : `2024-10`
- Le token Storefront dans le JS est public par design (read-only, scope limité)

## Dev local

Pas besoin de build. Ouvre directement `index.html` dans un navigateur ou sert avec :
```
python3 -m http.server 8080
```
