<script>
export default {
  name: "Compétences"
};
</script>

<template>
  <section class="skills section" id="skills">

    <div class="skills__container">          
      <div class="image_comp">
        <img 
          src="../assets/Competences.jpg" 
          alt="image d'un qlqn tapant sur un clavier" 
        />
        <div class="text_comp">
          <h2 class="skills__subtitle">Projet professionnelle</h2>
          <p>
            J'ai pu conquérir des connaissances côté Front-end notamment HTML, CSS, JavaScript et React.
            Suite à la formation, je continue à améliorer mes connaissances côté Front mais également côté Back
            avec des langages comme PHP, Symfony, SQL...
          </p>
          <div class="skills__data">
            <div class="skills__names">
                <i class='bx bxl-html5 skills__icon'></i>
                <span class="skills__name">HTML5</span>
            </div>
            <div class="skills__bar skills__html">

            </div>
            <div>
                <span class="skills__percentage">95%</span>
            </div>
        </div>
        <div class="skills__data">
          <div class="skills__names">
              <i class='bx bxl-css3 skills__icon'></i>
              <span class="skills__name">CSS3</span>
          </div>
          <div class="skills__bar skills__css">
              
          </div>
          <div>
              <span class="skills__percentage">85%</span>
          </div>
      </div>
      <div class="skills__data">
          <div class="skills__names">
              <i class='bx bxl-javascript skills__icon' ></i>
              <span class="skills__name">JAVASCRIPT</span>
          </div>
          <div class="skills__bar skills__js">
              
          </div>
          <div>
              <span class="skills__percentage">65%</span>
          </div>
      </div>
      <div class="skills__data">
          <div class="skills__names">
              <i class='bx bxs-paint skills__icon'></i>
              <span class="skills__name">React</span>
          </div>
          <div class="skills__bar skills__ux">
              
          </div>
          <div>
              <span class="skills__percentage">85%</span>
          </div>
      </div>
      <div class="skills__data">
        <div class="skills__names">
            <i class='bx bxl-javascript skills__icon' ></i>
            <span class="skills__name">PHP</span>
        </div>
        <div class="skills__bar skills__php">
            
        </div>
        <div>
            <span class="skills__percentage">50%</span>
        </div>
      </div>
      <div class="skills__data">
        <div class="skills__names">
            <i class='bx bxl-javascript skills__icon' ></i>
            <span class="skills__name">SQL</span>
        </div>
        <div class="skills__bar skills__SQL">
            
        </div>
        <div>
            <span class="skills__percentage">60%</span>
        </div>
      </div>
      <div class="skills__data">
        <div class="skills__names">
            <i class='bx bxl-javascript skills__icon' ></i>
            <span class="skills__name">Symfony</span>
        </div>
        <div class="skills__bar skills__symfony">
            
        </div>
        <div>
            <span class="skills__percentage">65%</span>
        </div>
      </div>
      </div>            
    </div>
    </div>
  </section>
</template>

<style scoped>
.title_comp {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 2em;
  font-size: 45px;
}


.skills__container {
  display: flex;
  justify-content: center;
  margin-top: 6em;
}


.image_comp {
  display: flex;
  align-items: center;
  gap: 2rem; 
}


.image_comp img {
  width: 450px;
  height: 550px;
  border-radius: 10px;
}


.text_comp {
  max-width: 450px;
}


.skills__subtitle {
  font-size: 28px;
  margin-left: -190px;
}

.text_comp p {
  font-size: 16px;
  line-height: 1.6;
  text-align: justify;
}

.skills__container {
  row-gap: 2rem;
  text-align: center;
}

.skills__subtitle {
  margin-bottom: var(--mb-2);
}

.skills__text {
  margin-bottom: var(--mb-4);
}

.skills__data {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
  font-weight: var(--font-semi);
  padding: 0.5rem 1rem;
  margin-bottom: var(--mb-4);
  border-radius: 0.5rem;
  box-shadow: 0px 4px 25px rgba(6, 153, 238, 0.15);
  margin-top: 1em;
}

.skills__icon {
  font-size: 2rem;
  margin-right: var(--mb-2);
  color: var(--first-color);
}

.skills__names {
  display: flex;
  align-items: center;
}

.skills__bar {
  position: absolute;
  left: 0;
  bottom: 0;
  background-color: var(--first-color);
  height: 0.25rem;
  border-radius: 0.5rem;
  z-index: var(--z-back);
}

.skills__html {
  width: 95%;
}

.skills__css {
  width: 85%;
}

.skills__js {
  width: 65%;
}

.skills__ux {
  width: 85%;
}

.skills__php {
  width: 50%;
}

.skills__SQL {
  width: 60%;
}

.skills__symfony {
  width: 65%;
}

.skills__img {
  border-radius: 0.5rem;
}


@media (max-width: 768px) {
  .image_comp {
    flex-direction: column;
    text-align: center;
  }

  .text_comp {
    max-width: 90%;
  }
}
</style>
