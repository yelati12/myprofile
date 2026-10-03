<script setup>
import Hero from './components/Hero.vue'
import Achievements from './components/Achievements.vue'
import Experience from './components/Experience.vue'
import Skills from './components/Skills.vue'
import Education from './components/Education.vue'
import Contact from './components/Contact.vue'
</script>

<template>
  <main class="app">

    <!-- Hero -->
    <Hero />

    <!-- Key Contributions -->
    <Achievements />

    <!-- Professional Experience -->
    <Experience />

    <!-- Technical Skills -->
    <Skills />

    <!-- Education -->
    <Education />

    <!-- Contact -->
    <Contact />

  </main>
</template>

<style scoped>
.app {
  width: 100%;
  min-height: 100vh;

  background: #ffffff;

  overflow-x: hidden;
}
</style>