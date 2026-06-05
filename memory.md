# Project Memory & Roadmap - LessGooo Hub

## État actuel (v1.9)
- **Pages fonctionnelles :** Accueil (`index.html`), FAQ (`FAQ.html`), Contact (`contact.html`), Qui sommes-nous (`about.html`).
- **Features déployées :**
    - Sélecteur de langue (FR/EN) fonctionnel sur toutes les pages.
    - Mode sombre/clair synchronisé et persistant.
    - Animation typewriter sur le hero de l'accueil.
    - Compteurs animés pour les statistiques (Focus : Réussite aux certifications).
    - Intégration WhatsApp (Bouton flottant et formulaire de contact direct sur `contact.html`).
    - Système de révélation au scroll (Animations CSS).
    - Catalogue multidisciplinaire (DevOps, CM, Web, Anglais, Allemand, Engins lourds) avec images dédiées pour chaque formation (`img10.png` pour CM, `img12.jpg` pour Web, `img13.jpg` pour Engins Lourds, `img14.jpg` pour Anglais Business, `img15.jpg` pour Allemand).
    - Footer inspirant et humain axé sur la communauté ("Chaque défi relevé").
    - Intégration Google Maps (Iframe) et lien d'itinéraire sur la page Contact.
    - Localisation précise : Bonabérie Mabandas (derrière la station BOCOM).
    - Diversification des témoignages pour refléter la variété des formations proposées.
    - Optimisation de la stabilité du header (logo, liens, bouton) pour éviter les décalages en mode sombre et lors du changement de langue.
    - Suppression des liens "Infrastructure" et "Blog" du menu de navigation.
    - Ajout d'une section "Notre Partenaire" avec le logo `easylearning.png` sur la page d'accueil.
    - Création d'une page dédiée "Qui sommes-nous" (`about.html`) avec son contenu déplacé de `index.html`.
    - Mise à jour du menu de navigation pour inclure et positionner "Qui sommes-nous" après "Learning Hub" sur toutes les pages.
    - Amélioration de la réactivité du menu de navigation sur la page "Qui sommes-nous".
    - Mise à jour de l'image de fond du héros de la page "Qui sommes-nous" avec `logo2.png` et effet de parallaxe.
    - Utilisation de `logo6.png` pour le logo du footer sur `index.html` pour une meilleure visibilité en mode sombre.
    - Ajout d'une section "À propos de la formation à LessGooo" sur `index.html` avec `img8.jpg` (image à gauche, texte à droite) et contenu textuel, avant les programmes SSP.
    - Mise à jour de l'image de la section "L'Esprit LessGooo Hub" sur `about.html` avec `img7.jpg`.
    - Correction du décalage du menu sur `contact.html` pour qu'il soit cohérent avec les autres pages.
    - Amélioration du formulaire de contact : remplacement du champ "Sujet" par une liste déroulante (`select`) proposant les différentes formations.
    - Adaptation de la `FAQ.html` pour couvrir toutes les formations proposées.
    - Correction de la réactivité de la page "Qui sommes-nous" (`about.html`) et harmonisation du menu mobile.
    - Optimisation du menu mobile : le "Learning Hub" est désormais escamotable (toggle) et le menu se ferme automatiquement lors d'un clic sur un lien.
    - Harmonisation du menu de navigation sur `FAQ.html` : remplacement de "Formations" par "Learning Hub" dans les traductions.
    - Correction du bug d'affichage de l'image `img8.jpg` sur `index.html`.

## Dette technique & Problèmes connus
- **Maintenance i18n :** Les traductions sont stockées directement dans le script JS de chaque page. Cela deviendra ingérable avec l'augmentation du contenu.
- **Header/Footer :** Actuellement dupliqués en dur dans chaque fichier HTML. Toute modification nécessite une mise à jour sur toutes les pages.
- **Cohérence du logo du footer :** Le logo du footer est actuellement `logo1.jpg` dans `index.html` mais le JS de `about.html` et `FAQ.html` le force à `logo1.jpg` ou `logo2.png` selon le thème. Il faut harmoniser cela pour qu'il reste `logo1.jpg` ou `logo6.png` comme décidé, sans être affecté par le thème.

## Améliorations de code suggérées (à considérer)
- **CSS :**
    - Centraliser les styles CSS communs dans un fichier externe (`styles.css`).
    - Utiliser des classes utilitaires pour les paddings/margins au lieu de styles inline.
- **HTML :**
    - Ajouter des attributs `loading="lazy"` aux images pour optimiser les performances.
    - Revoir la structure du menu déroulant pour une meilleure accessibilité (ARIA attributes).
- **JavaScript :**
    - Refactoriser le code JavaScript pour le thème et la langue afin d'éviter la duplication sur chaque page.

## Prochaines étapes (Todo List)
### Court terme
- [ ] Extraire le JavaScript commun dans un fichier `assets/js/app.js`.
- [ ] Centraliser le CSS dans un dossier `assets/css/` (styles.css, components.css, theme.css).
- [ ] Implémenter un système d'inclusion de composants (Header/Footer) via JS ou un mini-générateur de site statique.

### Moyen terme
- [ ] Déplacer les traductions dans des fichiers JSON externes.
- [ ] Configurer un pipeline CI/CD (GitHub Actions) pour le déploiement automatique.
- [ ] Optimiser les images (conversion en `.webp`).

### DevOps / Infrastructure
- [ ] Dockeriser l'environnement de développement pour inclure un serveur Nginx de test.
- [ ] Mettre en place un monitoring simple (UptimeRobot) une fois en ligne.