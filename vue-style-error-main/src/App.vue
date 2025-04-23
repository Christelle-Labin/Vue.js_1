<script setup>
// Import du tableau contenant la liste des animaux
import data from './assets/data.json'

// Import du composant
import AppCard from './components/AppCard.vue'
</script>

<template>
  <main>
    <h1>Animals for adoption</h1>

    <div class="container">
      <!-- Appel du composant 10 fois : une fois par animal -->
      <AppCard :animalInfos="data[0]" />
      <AppCard :animalInfos="data[1]" />
      <AppCard :animalInfos="data[2]" />
      <AppCard :animalInfos="data[3]" />
      <AppCard :animalInfos="data[4]" />
      <AppCard :animalInfos="data[5]" />
      <AppCard :animalInfos="data[6]" />
      <AppCard :animalInfos="data[7]" />
      <AppCard :animalInfos="data[8]" />
      <AppCard :animalInfos="data[9]" />
    </div>
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 50px;
  background-color: var(--bgc-main);
  min-height: 100vh;
}
main > div {
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  flex: 1;
}

/* RWD */
@media (max-width: 1098px) {
  main > div {
    flex-wrap: wrap;
    justify-content: center;
  }
}
</style>
