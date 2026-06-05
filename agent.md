# Agent Context & Project Constraints - LessGooo Hub

## Description du projet
**LessGooo Learning Hub** est une plateforme multidisciplinaire dédiée à l'acquisition de compétences métiers (Self-Study Program - SSP). Elle couvre le DevOps/Cloud, le marketing digital (Community Management), le développement Web, les langues (Anglais/Allemand) et les métiers techniques (Conduite d'engins lourds). Le projet favorise l'échange entre pairs et l'insertion professionnelle.

**Public cible :** Étudiants, professionnels en reconversion, techniciens et toute personne souhaitant monter en compétences sur des métiers porteurs.
**Valeur ajoutée :** Apprentissage hybride (théorie et pratique intensive), mentorat communautaire et préparation aux certifications internationales.

## Architecture & Stack Technique
- **Frontend :** HTML5, CSS3 (Variables personnalisées pour le thèming), JavaScript Vanilla (ES6+).
- **UI/UX :** FontAwesome 6.4.0 pour l'iconographie, Google Fonts (Inter) pour la typographie.
- **Logic :** Système i18n (Internationalisation) personnalisé géré via `localStorage` et attributs `data-i18n`.
- **Thème :** Système Dual-theme (Light/Dark) persistant via `localStorage`.
- **Infrastructure :** Actuellement conçu pour un déploiement statique (Nginx, S3, GitHub Pages).

## Contraintes techniques
- **Performance :** Temps de chargement minimal requis (limitation des bibliothèques externes).
- **Compatibilité :** Responsive Design strict (Mobile-first) avec support des navigateurs modernes.
- **Environnement :** Développement local possible sans serveur de build, mais prêt pour une intégration dans un pipeline CI/CD (GitHub Actions).
- **Sécurité :** Validation côté client pour les formulaires de contact (WhatsApp integration).

## Règles de code
- **CSS :** Utilisation intensive des variables CSS (`:root`) pour maintenir la cohérence visuelle.
- **Naming :** Conventions claires pour les classes (ex: `faq-item`, `nav-link`).
- **JavaScript :** 
    - Fonctions pures autant que possible.
    - Manipulation directe du DOM sans framework.
    - Isolation des données de traduction dans des objets `translations`.
- **Git :**
    - Commits explicites en français ou anglais.
    - Branches : `main` (production), `develop` (features).