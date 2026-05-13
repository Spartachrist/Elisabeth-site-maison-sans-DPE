# CLAUDE.md — Site de vente "La Ferme de la Vallée d'Or" — VARIANTE PRIVÉE SANS DPE

> Document de contexte pour Claude Code. À lire en début de chaque session.

## 🎯 Contexte du projet

**Variante PRIVÉE** du site one-page de vente de la ferme pyrénéenne d'**Elisabeth Goddet**, **sans la section énergie** (DPE, GES, aides à la rénovation) et **sans la section "Détail des pièces"** (tableau loi Carrez avec les 16 espaces).

### Pourquoi cette variante ?

Des changements récents sur le bien rendent le DPE actuel (classe G, diagnostic du 17/03/2025) non représentatif. En attendant un nouveau diagnostic, Elisabeth utilise deux versions du site :

- **Version publique « avec DPE »** : repo `Spartachrist/Elisabeth-Site-Maison`, URL `ferme-a-vendre-pyrenees.vercel.app`. Figée, ne sera plus modifiée.
- **Version privée « sans DPE » (CE REPO)** : partagée en 1-to-1 par Elisabeth après communication verbale du DPE.

### Caractéristiques techniques

- **HTML/CSS/JS pur** — un seul fichier `index.html`, pas de framework, pas de build
- **Non indexée** : `robots.txt` (Disallow: /) + meta `noindex,nofollow`
- **Hébergement** : Vercel (auto-deploy sur push `main`)
- **URL prod** : `https://ferme-pyrenees-prive.vercel.app/` (à adapter si autre nom de projet Vercel)
- **Formulaire de contact** : Web3Forms, clé identique au site public
- **Polices** : Cormorant Garamond + Jost via Google Fonts

### Bien

- Adresse : 41 Route de Saint-Arroman, 65250 Hèches, Hautes-Pyrénées
- Prix : 237 000 € (vente entre particuliers)
- Surface : 300 m² habitables (loi Carrez) + 200 m² de dépendances + 4 400 m² de terrain
- Email de contact affiché : `lisalang@laposte.net`

## 📂 Structure du projet

```
.
├── CLAUDE.md       (ce fichier)
├── index.html      (page unique, ≈ 45 KB)
├── robots.txt      (Disallow: /)
├── vercel.json     (headers de sécurité)
└── images/         (toutes les photos)
```

## ⚠️ Points de vigilance

### 1. Ne JAMAIS rajouter la section DPE ni la section "Détail des pièces"

Toute la chaîne DPE (HTML section, CSS .dpe-*, nav link, footer mention, JSON-LD) ainsi que la chaîne "Pièces" (section HTML, CSS .pieces-*/.logement-*, nav link) ont été volontairement retirées. La raison existe : la version publique est là pour ça. Cette variante est faite pour être partagée à des prospects qui ont déjà reçu l'info DPE et le détail des pièces verbalement.

### 2. Ne jamais désactiver la non-indexation

`robots.txt` + meta `noindex` sont la mitigation légale principale. Ne jamais retirer.

### 3. Indépendance vis-à-vis du repo principal

Ce repo n'a aucun lien git avec `Spartachrist/Elisabeth-Site-Maison`. Le repo principal est figé. Toute modification ici reste ici.

### 4. Conventions de code (identiques au repo principal)

- HTML/CSS minifié-style (lignes denses)
- Tous les styles dans `<style>` inline du `<head>`
- Tout le JS dans `<script>` en fin de body, vanilla JS
- Pas d'emojis dans le code sauf demande explicite

## 📞 Liens utiles

- Repo GitHub : https://github.com/Spartachrist/Elisabeth-site-maison-sans-DPE
- Site déployé : https://ferme-pyrenees-prive.vercel.app/ (à adapter)
- Repo du site public (référence figée) : https://github.com/Spartachrist/Elisabeth-Site-Maison
- Web3Forms dashboard : https://web3forms.com
- Vercel dashboard : https://vercel.com
