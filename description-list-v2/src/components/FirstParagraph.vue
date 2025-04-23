<script setup>
defineProps({
  gender: String,
  age: Number,
  job: String,
})
const getPronoun = (gender, type) => {
  if (type === 'subject') return gender === 'female' ? 'She' : 'He'
}
</script>

<template>
  <p>{{ getPronoun(gender, 'subject') }} is a {{ age }}-year-old {{ job.toLowerCase() }}.</p>
</template>
