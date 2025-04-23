<script setup>
const props = defineProps({
  gender: String,
  pet: Object,
})
console.log(props.personInfos)

const getPronoun = (gender, type) => {
  if (type === 'possessivePronoun') return gender === 'female' ? 'her' : 'his'
}
</script>

<template>
  <p>
    At home, {{ getPronoun(gender, 'possessivePronoun') }} lively companion is {{ pet.name }} a
    {{ pet.age }}-years-old {{ pet.species }}.
  </p>
</template>
