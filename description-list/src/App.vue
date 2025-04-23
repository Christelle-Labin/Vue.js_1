<script setup>
const firstPerson = {
  gender: 'female',
  firstname: 'Emily',
  lastname: 'Parker',
  age: 24,
  job: 'Teacher',
  hobbies: ['read books', 'go hiking'],
  pet: {
    name: 'Whiskers',
    age: 2,
    species: 'ferret',
  },
}

const secondPerson = {
  gender: 'male',
  firstname: 'Marcus',
  lastname: 'Bennett',
  age: 38,
  job: 'Architect',
  hobbies: ['watch bird', 'play chess'],
  pet: {
    name: 'Nala',
    age: 6,
    species: 'dog',
  },
}

const thirdPerson = {
  gender: 'female',
  firstname: 'Sophia',
  lastname: 'Rodriguez',
  age: 31,
  job: 'Environmental scientist',
  hobbies: ['play guitar', 'bake cakes'],
  pet: {
    name: 'Paws',
    age: 3,
    species: 'cat',
  },
}

const fourthPerson = {
  gender: 'male',
  firstname: 'Oliver',
  lastname: 'Hughes',
  age: 56,
  job: 'Carpenter',
  hobbies: ['paint', 'ride horses'],
  pet: {
    name: 'Bubble',
    age: 4,
    species: 'snake',
  },
}
const getPronoun = (gender, type) => {
  if (type === 'subject') return gender === 'female' ? 'She' : 'He'
  if (type === 'possessivePronoun') return gender === 'female' ? 'her' : 'his'
  return ''
}
</script>

<template>
  <main>
    <h1>Description list</h1>
    <div class="container">
      <!---------- card-1 --------->
      <section class="card">
        <img src="/src/assets/pictures/emily-parker.jpg" alt="Emily Parker" />
        <div class="content">
          <h2>{{ `${firstPerson.firstname} ${firstPerson.lastname}` }}</h2>
          <p>
            {{ getPronoun(firstPerson.gender, 'subject') }} is a {{ firstPerson.age }}-year-old
            {{ firstPerson.job.toLowerCase() }}.
          </p>
          <p>
            Outside of work, {{ firstPerson.firstname }} likes to {{ firstPerson.hobbies[0] }} and
            {{ firstPerson.hobbies[1] }}.
          </p>
          <p>
            At home, {{ getPronoun(firstPerson.gender, 'possessivePronoun') }} lively companion is
            {{ firstPerson.pet.name }} a {{ firstPerson.pet.age }}-years-old
            {{ firstPerson.pet.species }}.
          </p>
        </div>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </section>

      <!---------- card-2 --------->
      <section class="card">
        <img src="/src/assets/pictures/marcus-bennett.jpg" alt="Marcus Bennett" />
        <div class="content">
          <h2>{{ `${secondPerson.firstname} ${secondPerson.lastname}` }}</h2>
          <p>
            {{ getPronoun(secondPerson.gender, 'subject') }} is a {{ secondPerson.age }}-year-old
            {{ secondPerson.job.toLowerCase() }}.
          </p>
          <p>
            Outside of work, {{ secondPerson.firstname }} likes to {{ secondPerson.hobbies[0] }} and
            {{ secondPerson.hobbies[1] }}.
          </p>
          <p>
            At home, {{ getPronoun(secondPerson.gender, 'possessivePronoun') }} lively companion is
            {{ secondPerson.pet.name }} a {{ secondPerson.pet.age }}-years-old
            {{ secondPerson.pet.species }}.
          </p>
        </div>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </section>

      <!---------- card-3 --------->
      <section class="card">
        <img src="/src/assets/pictures/sophia-rodriguez.jpg" alt="Sophia Rodriguez" />
        <div class="content">
          <h2>{{ `${thirdPerson.firstname} ${thirdPerson.lastname}` }}</h2>
          <p>
            {{ getPronoun(thirdPerson.gender, 'subject') }} is a {{ thirdPerson.age }}-year-old
            {{ thirdPerson.job.toLowerCase() }}.
          </p>
          <p>
            Outside of work, {{ thirdPerson.firstname }} likes to {{ thirdPerson.hobbies[0] }} and
            {{ thirdPerson.hobbies[1] }}.
          </p>
          <p>
            At home, {{ getPronoun(thirdPerson.gender, 'possessivePronoun') }} lively companion is
            {{ thirdPerson.pet.name }} a {{ thirdPerson.pet.age }}-years-old
            {{ thirdPerson.pet.species }}.
          </p>
        </div>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </section>

      <!---------- card-4 --------->
      <section class="card">
        <img src="/src/assets/pictures/olivier-hughes.jpg" alt="Olivier Hugues" />
        <div class="content">
          <h2>{{ `${fourthPerson.firstname} ${fourthPerson.lastname}` }}</h2>
          <p>
            {{ getPronoun(fourthPerson.gender, 'subject') }} is a {{ fourthPerson.age }}-year-old
            {{ fourthPerson.job.toLowerCase() }}.
          </p>
          <p>
            Outside of work, {{ fourthPerson.firstname }} likes to {{ fourthPerson.hobbies[0] }} and
            {{ fourthPerson.hobbies[1] }}.
          </p>
          <p>
            At home, {{ getPronoun(fourthPerson.gender, 'possessivePronoun') }} lively companion is
            {{ fourthPerson.pet.name }} a {{ fourthPerson.pet.age }}-years-old
            {{ fourthPerson.pet.species }}.
          </p>
        </div>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </section>
    </div>
  </main>
</template>

<style scoped>
main {
  width: 100vw;
  height: 100vh;
  box-sizing: border-box;
  font-family: Helvetica, sans-serif;
  overflow-x: hidden;
  background-color: #c9e1c2;
  border-radius: 10px;
  padding-bottom: 2rem;
}
h1 {
  font-size: 2.4rem;
  font-weight: bold;
  color: white;
  text-align: center;
  letter-spacing: 0.1em;
  padding: 3rem 1rem 2rem;
}
.container {
  display: flex;
  justify-content: space-between;
  gap: 1.5rem;
  padding: 0 2rem;
}
.card {
  width: 100%;
  max-width: 250px;
  height: 380px;
  margin: 0;
  margin-bottom: 1.25rem;
  padding: 1.25rem;
  background-color: white;
  border-radius: 10px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.3);
  display: flex;
  flex-direction: column;
}
.card img {
  height: 150px;
  width: 250px;
  display: block;
  margin: 0 auto;
  object-fit: cover;
  border-radius: 5px;
}
.content {
  width: 100%;
  align-items: center;
  margin-top: 1rem;
}
.content h2 {
  font-size: 1.2rem;
  font-weight: bold;
  margin-top: 0.5rem;
}
p {
  margin-top: 0.75rem;
  font-size: 0.95rem;
  line-height: 1.2;
}
svg {
  color: gray;
  align-self: flex-end;
  margin-top: 20px;
}
.card:nth-child(3) svg {
  margin-top: 5px;
}

/* RWD */
@media (max-width: 1300px) {
  .container {
    flex-wrap: wrap;
    justify-content: center;
  }

  .card {
    max-width: 250px;
  }
}
@media (max-width: 768px) {
  h1 {
    font-size: 2rem;
  }
  .container {
    flex-direction: column;
    align-items: center;
  }

  .card {
    width: 90%;
  }
}
</style>
