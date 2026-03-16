<script setup>
import Home from "./components/Home.vue";
import Apropos from "./components/Apropos.vue";
import Projets from "./components/Projets.vue";
import Competences from "./components/Compétences.vue";
import Contact from "./components/Contact.vue";
import Footer from "./components/Footer.vue";
import NotFound from "./components/NotFound.vue";

import { ref, computed } from "vue";

const routes = {
  '/': Home,
  '/apropos': Apropos,
  '/competences': Competences,
  '/projets': Projets,
  '/contact': Contact
}

const currentPath = ref(window.location.hash.slice(1) || '/')

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash.slice(1) || '/'
})

const currentView = computed(() => {
  return routes[currentPath.value] || NotFound
})

</script>

<template>
  <div class="app">
    <nav class="navbar">
      <div class="logo">
        <a href="#/">Sulayman</a>
      </div>
      <ul class="nav-links" >
        <li><a href="#/">Home</a></li>
        <li><a href="#/apropos">A propos</a></li>
        <li><a href="#/competences">Competences</a></li>
        <li><a href="#/projets">Projets</a></li>
        <li><a href="#/contact">Contact</a></li>
      </ul>
    </nav>

    <main class="main-content">
      <Transition>
        <component :is="currentView" />
      </Transition>
    </main>

    <Footer />
  </div>
</template>

<style scoped>

.v-enter-active {
  transition: opacity 2s ease;
}

.v-enter-from {
  opacity: 0;
}

.app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.main-content {
  flex: 1;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #333;
  padding: 0.5em 1em;
  color: white;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 3em;
  margin: 0;
  cursor: pointer;
}

.nav-links a {
  text-decoration: none;
  color: white;
}

.nav-links a:hover {
  color: #00bfff;
  transition: color 0.3s;
}

.logo a {
  text-decoration: none;
  color: white;
  cursor: pointer;
  list-style: none;
}

.logo a:hover {
  color: #00bfff;
  list-style: none;
  transition: color 0.3s;
}

@media (max-width: 680px) {
  .nav-links {
    flex-direction: column;
    gap: 1em;
  }
}

</style>
