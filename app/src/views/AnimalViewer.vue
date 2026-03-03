<script setup>
const animals = ref([
  { name: 'Leo', species: 'Lion', weight: 420 },
  { name: 'Ella', species: 'Elephant', weight: 5000 },
  { name: 'Max', species: 'Dog', weight: 30 },
  { name: 'Whiskers', species: 'Cat', weight: 4 },
  { name: 'Bubbles', species: 'Fish', weight: 0.5 },
  { name: 'Charlie', species: 'Horse', weight: 500 },
  { name: 'Hoppy', species: 'Rabbit', weight: 3 },
  { name: 'Tweety', species: 'Bird', weight: 0.2 },
  { name: 'Gerry', species: 'Giraffe', weight: 1200 },
  { name: 'Bella', species: 'Bear', weight: 300 },
])

import { ref } from 'vue'
import AnimalCard from '@/components/AnimalCard.vue'
</script>

<template>
  <div>
    <AnimalCard v-for="animal in animals" :key="animal.name" :animal="animal">
      {{ animal.name }}</AnimalCard
    >
  </div>
</template>

<style lang="css" scoped>
div {
  padding: 16px;
}

h1 {
  text-align: center;
  margin-bottom: 20px;
}
.container {
  display: flex;
  width: 80vw;
  margin: 20px auto;
  justify-content: space-around;
  align-items: center;
  flex-wrap: wrap;
}
.card {
  border: 1px solid #ccc;
  padding: 12px;
  margin-bottom: 12px;
  border-radius: 6px;
  width: 300px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}
</style>
