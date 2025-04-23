<script setup>
import AppPresentation from './AppPresentation.vue'
// Déclaration de la props qui contient les informations d'un animal
defineProps({
  animalInfos: Object
})
</script>

<template>
  <div :class="['card', { isInactive: animalInfos.alreadyAdopted }]">
    <!-- <div :class="{ opacity: animalInfos.alreadyAdopted }"> -->
    <div>
      <AppPresentation :animalInfos="animalInfos" />
    </div>
    <p class="description">{{ animalInfos.description }}</p>
  </div>
</template>

<style scoped>
.card {
  background-color: var(--bgc-card);
  padding: 15px;
  border-radius: 5px;
  width: calc((100% - 15px) / 2);
  display: flex;
  flex-direction: row;
  gap: 10px;
  box-shadow: var(--box-sdw);
}
div {
  width: 150px;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  gap: 10px;
}
.isInactive {
  opacity: 0.4;
  filter: grayscale(0.4);
  cursor: not-allowed;
}
.description {
  flex: 1;
}

@media (max-width: 998px) {
  .card {
    width: 100%;
  }
  .description {
    flex: inherit;
  }
}
</style>
