<script setup>
import AppTitle from './AppTitle.vue'
import FirstParagraph from './FirstParagraph.vue'
import SecondParagraph from './SecondParagraph.vue'
import ThirdParagraph from './ThirdParagraph.vue'

defineProps({
  personInfos: Object,
})
</script>

<template>
  <section>
    <img
      src="https://res.cloudinary.com/lereacteur-apollo/image/upload/v1704967000/RNCP31114/cours-vue/exo-sem-1/mystery-person_bueack.jpg"
      alt="mystery avatar"
    />

    <div>
      <AppTitle
        :firstname="personInfos.firstname"
        :lastname="personInfos.lastname"
        :gender="personInfos.gender"
      />

      <FirstParagraph :gender="personInfos.gender" :age="personInfos.age" :job="personInfos.job" />

      <SecondParagraph :firstname="personInfos.firstname" :hobbies="personInfos.hobbies" />

      <ThirdParagraph :gender="personInfos.gender" :pet="personInfos.pet" />
    </div>

    <font-awesome-icon :icon="['fas', 'heart']" />
  </section>
</template>

<style scoped>
section {
  flex: 1;
  background-color: #eeeeee;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0px 4px 10px v-bind('personInfos.favoriteColor');
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

section img {
  width: 100%;
  display: block;
  margin-bottom: 20px;
  object-fit: cover;
  object-position: top;
  border-radius: 5px;
}
svg {
  color: gray;
  align-self: flex-end;
  margin-top: 20px;
}
/* ------------ RWD ------------ */
@media (max-width: 998px) {
  section {
    flex: none;
    width: 250px;
  }
}
</style>
