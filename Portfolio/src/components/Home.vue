<script>
export default {
  name: "Home"
};
</script>

<template>
  <div class="accueil">
      <h2 class="title">Bonjour, Sulayman Développeur web en Formation CDA</h2><br></br>
      <img src="https://sulayman2005.github.io/Portfolio_final/assets/img/Sulayman_preview.webp" alt="image de Sulayman" class="image_sulayman"></img>
      <p class="description">Développeur web / CDA</p>
  </div>
</template>

<style scoped>
.accueil {
    display: flex;
    margin-top: 50px;
}

.title {
    display: flex;
    flex-direction: column;
    gap: 1em;
    font-size: 30px;
}

.image_sulayman {
  position: absolute;
  right: 0;
  margin-right: 120px;
  width: 200px;
}

.description {
    position: absolute;
    margin-top: 100px;
}

@media (max-width: 1125px) {
  .description {
    margin-top: 490px;
  }
  .accueil img {
    display: flex;
    position: absolute;
    left: 0;
    margin-top: 9em;
    margin-left: 120px;
  }
}

</style>