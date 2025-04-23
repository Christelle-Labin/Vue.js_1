<script setup>
// Déclaration de la props qui contient les informations d'un animal
defineProps({
  animalInfos: Object
})
</script>

<template>
  <h2>
    {{ animalInfos.name }}
    <!-- Ajout badge "Adopté" -->
    <span v-if="animalInfos.alreadyAdopted" class="badge">Adopté</span>
  </h2>
  <p><span>Espèce</span> : {{ animalInfos.species }}</p>
  <p><span>Age</span> : {{ animalInfos.age }}</p>
</template>

<style scoped>
p {
  color: var(--clr-p);
}
span {
  text-decoration: underline;
  color: var(--clr-span);
}
.badge {
  background-color: var(--bgc-badge);
  color: var(--neutral-clr);
  font-size: 0.7rem;
  padding: 2px 6px;
  border-radius: 10px;
  margin-left: 8px;
  text-transform: uppercase;
  font-weight: bold;
}
</style>
