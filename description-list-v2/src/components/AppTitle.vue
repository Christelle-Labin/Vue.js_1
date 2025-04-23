<script setup>
defineProps({
  gender: String,
  firstname: String,
  lastname: String,
})
</script>

<template>
  <h2 :class="{ isActive: gender === 'female' }">{{ `${firstname} ${lastname}` }}</h2>
</template>

<style scoped>
.isActive {
  color: orange;
}
</style>
