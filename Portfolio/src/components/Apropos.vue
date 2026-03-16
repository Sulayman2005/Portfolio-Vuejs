<script>
export default {
  name: "A propos"
};

</script>

<template>
  <div class="page_apropos">
    <div class="apropos_container">
      <img
        src="https://sulayman2005.github.io/Portfolio_final/assets/img/picture_dev_preview.webp"
        alt="image d'un ordi de développeur"
        class="image_pc"
      />

      <div class="block_textApropos">
        <h2 class="prenom">Sulayman</h2>
        <p class="about__text">
          J’ai suivi une formation de développeur web d’une durée de 9 mois, durant laquelle j’ai acquis les bases du développement web, notamment côté front-end. En complément, j’ai développé des compétences en no-code, en utilisant des outils comme WordPress et Webflow pour améliorer le design et l’ergonomie des interfaces.
          <br /><br />
          En dehors de ma formation, j’ai également pris l’initiative d’effectuer plusieurs stages dans le domaine du web, ce qui m’a permis de renforcer mes compétences sur le terrain et de mieux comprendre les attentes du milieu professionnel.
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.page_apropos {
  margin-top: 120px;
  text-align: center;
}

.apropos_container {
  display: flex;
  align-items: center; 
  justify-content: center;
  gap: 2rem; 
  flex-wrap: wrap;
  margin-top: 2rem;
}

.image_pc {
  width: 300px;
  max-width: 100%;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}

.block_textApropos {
  max-width: 600px;
  text-align: left;
}

.prenom {
  font-weight: bold;
  margin-bottom: 1rem;
}

.about__text {
  line-height: 1.6;
}

@media (max-width: 768px) {
  .apropos_container {
    flex-direction: column;
    text-align: center;
  }

  .block_textApropos {
    text-align: center;
  }
}
</style>
