<script setup>
import About from './components/About.vue';
import Hero from './components/Hero.vue';
import Navigation from './components/Navigation.vue';
import Projects from './components/Projects.vue';
import Skills from './components/Skills.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';

</script>

<template>
  <Navigation />
  <Hero msg="Vite + Vue" />
  <About msg="Vite + Vue" />
  <Skills />
  <Projects />
  <Contact />
  <Footer />

</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
