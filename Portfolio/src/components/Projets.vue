<script>
export default {
  name: "Projets",
  data() {
    return {
      projets: [
        {
          id: 1,
          nom: "Ohmyfood",
          lien: "https://github.com/Sulayman2005/Canteau_Sulayman_P4_ohmyfood",
          image: "/Ohmyfood(1).png",
          description:
            "Création d’un site mobile-first de menus interactifs pour des restaurants à Paris. Intégration HTML/CSS poussée avec animations.",
          stack: ["HTML", "SASS", "CSS3"],
        },
        {
          id: 2,
          nom: "Sophie Bluel",
          lien: "https://github.com/Sulayman2005/Page_web_dynamique_javascript",
          image: "/Sophie Bluel(1).png",
          description:
            "Développement d'une page web dynamique avec JavaScript vanilla. Intégration d’un système de filtres interactifs pour une galerie.",
          stack: ["HTML", "CSS", "JavaScript"],
        },
        {
          id: 3,
          nom: "Kasa",
          lien: "https://github.com/Sulayman2005/Application-web-React",
          image: "/projet kasa(1).png",
          description:
            "Création d’une application web React affichant des logements. Utilisation de React Router et composants dynamiques.",
          stack: ["React", "JavaScript", "CSS"],
        },
        {
          id: 4,
          nom: "Nina Carducci (SEO)",
          lien: "https://github.com/Sulayman2005/Projet-nina-carducci",
          image: "/SEO.PNG",
          description:
            "Optimisation SEO et accessibilité d’un site existant. Travail sur les performances, structure sémantique, et métadonnées.",
          stack: ["HTML", "CSS", "Lighthouse", "SEO"],
        },
        {
          id: 5,
          nom: "Déboggage d’application",
          lien: "https://github.com/Sulayman2005/debuggez_application",
          image: "/Débuggage.PNG",
          description:
            "Débogage et correction d’une application JavaScript existante. Résolution de bugs liés aux formulaires et aux appels API.",
          stack: ["JavaScript", "Chrome DevTools"],
        },
        {
          id: 6,
          nom: "Argent Bank",
          lien: "https://github.com/Sulayman2005/Aregnt_Bank",
          image: "/argent bank(1).png",
          description:
            "Implémentation du front-end d’une application bancaire avec React et Redux. Authentification, gestion de session et données utilisateurs.",
          stack: ["React", "Redux", "JavaScript", "API REST"],
        },
        {
          id: 7,
          nom: "Project Fil Rouge",
          lien: "https://github.com/Sulayman2005/project_fil_rouge",
          image: "/projet_fil_rouge(1).png",
          description:
            "Implémentation sur un projet de base sur le début de ma formation CDA pour connaître mes bases en développement.",
          stack: ["React", "Vite"],
        },
        {
          id: 8,
          nom: "Site de Recettes",
          lien: "https://github.com/Sulayman2005/site_recettes",
          image: "/boutique_ligne(1)(1).png",
          description:
            "Initialisation à PHP avec un site de recettes avec une base de données et un back en PHP.",
          stack: ["PHP", "SQL"],
        },
        {
          id: 9,
          nom: "Mini Twitter",
          lien: "https://github.com/Sulayman2005/Mini-Twitter",
          image: "/Twitter (2).png",
          description:
            "Projet de groupe avec un Mini Twitter avec beaucoup de stack côté back mais également côté front-end.",
          stack: ["PHP", "SQL"],
        },
      ],
    };
  },
};
</script>


<template>

<section class="work__section">
    <div class="work__container">
        <div v-for="projet in projets" :key="projet.id" class="work__item">
            <a :href="projet.lien" class="work__img" :alt="projet.nom">
              <img :src="projet.image" :alt="projet.nom" loading="lazy">
            </a>
            <p class="description_work">{{ projet.description }}</p>
            <p>
              <em>Stack :</em> 
              {{ projet.stack.join(' , ') }}
            </p>
        </div>
    </div>
</section>

</template>

<style>

.title_projets {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 2em;
  font-size: 45px;
}

.description_work {
  display: flex;
  flex-wrap: wrap;
  min-width: 10px;
}

.work__container {
  margin-top: 5em;
  margin-left: 5em;
  column-count: 3; 
  gap: 9em;
}

.work__container img:hover {
  animation-duration: 1s;
}

.work__item {
  break-inside: avoid; 
  margin-bottom: 40px;
  font-size: 15px;
}

@media (max-width: 1400px) {
  .work__container {
    column-count: 2; 
  }
}

@media (max-width: 768px) {
  .work__container {
    column-count: 1; 
  }
}

@media (max-width: 568px) {
  .work__img img {
    font-size: 8px;
  }
}

</style>
