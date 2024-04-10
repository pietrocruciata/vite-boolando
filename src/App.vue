<script setup>
import NavBar from './components/NavBar.vue'
import MainSection from './components/MainSection.vue'
import FooterSection from './components/FooterSection.vue'
</script>

<template>

  <NavBar />
  <MainSection />
  <FooterSection />
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
