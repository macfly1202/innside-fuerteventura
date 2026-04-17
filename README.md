# INNSiDE Fuerteventura Suite

Guide éditorial indépendant de l'INNSiDE by Meliá Fuerteventura.
Site web cinématique, SEO/GEO optimisé, prêt pour déploiement Netlify.

## Structure

```
.
├── index.html              # Site principal (88 KB, 15 sections)
├── photos/                 # 22 médias : 17 photos + 2 vidéos + 3 posters
├── llms.txt                # Index court pour crawlers LLM (Answer.AI convention)
├── llms-full.txt           # Version longue pour ingestion LLM
├── robots.txt              # AI crawlers explicitement autorisés
├── sitemap.xml             # Sitemap canonique + image sitemap étendu
├── _headers                # Config cache + security Netlify
├── humans.txt              # Crédits auteurs (signal d'autorité)
└── README.md               # Ce fichier
```

## Déploiement

### Option A — drop dans repo Git existant

```bash
cd /Users/jmp/Downloads/INNSiDE_Fuerteventura_Suite
# copier les fichiers par-dessus la version actuelle
git add -A
git commit -m "snapshot complet: site + GEO + vidéos"
git push
```

### Option B — nouveau deploy Netlify

1. Décompresser le ZIP
2. Drop sur https://app.netlify.com/drop
3. Domain settings → brancher un domaine si besoin

## Caractéristiques techniques

- HTML/CSS/JS vanilla, aucune dépendance runtime
- Fonts : Fraunces + Archivo + Italiana (Google Fonts CDN)
- Design : cinéma immersif dark-mode, accents or
- Scroll : natif fluide
- Vidéo : autoplay via IntersectionObserver, pause hors-viewport
- Accessibilité : prefers-reduced-motion respecté
- SEO/GEO : JSON-LD graph (8 entités), 10 FAQ schema, llms.txt convention
- Poids total : ~14 MB (optimisé pour Lighthouse 90+)

## Structured data (JSON-LD)

Types présents dans index.html :
- Article (positionnement éditorial)
- Hotel (44 attributs + aggregateRating + reviews)
- HotelRoom (The Studio vue mer)
- Beach (Sotavento, avec Wikidata)
- TouristAttraction (René Egli)
- Place (Jandía, avec Wikidata)
- FAQPage (10 questions canoniques)
- BreadcrumbList

## Validation

Après déploiement :
- Rich Results Test : https://search.google.com/test/rich-results
- Schema validator : https://validator.schema.org/
- OG inspector : https://www.opengraph.xyz/

## Licence

Contenu éditorial original. Photos : mix photos personnelles (JMP, 2025) + images Meliá DAM (usage éditorial).
Non-affilié à Meliá Hotels International.

---
Généré le 17 avril 2026.
