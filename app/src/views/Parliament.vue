<template>
  <div class="container">
    
        <RouterLink to="/">Return to the home screen</RouterLink>
    <img class="subContainer" src="/parliament.png" />
    <div class="container">
      <div v-if="showMemberVariable === true">
        <button @click="showMembers()">
          Click here to hide the list of top Members of Parliament
        </button>
        <div class="subContainer" v-for="mp in mps">{{ mp.name }}, {{ mp.party }}</div>
      </div>
      <div v-else>
        <button @click="showMembers()">
          Click here to show the list of top Members of Parliament
        </button>
        <div>We currently have yet to see any members of parliament</div>
      </div>
    </div>
  </div>
  
</template>

<script setup>
import { ref } from 'vue'

let showMemberVariable = ref(false)
let showMembersInteger = ref(0)

function showMembers() {
  console.log('Old showMembersInteger value: ' + showMembersInteger.value)
  showMembersInteger.value++
  console.log('New showMembersInteger value: ' + showMembersInteger.value)
  if (showMembersInteger.value % 2 != 0) {
    showMemberVariable.value = true
    return showMemberVariable
  } else {
    showMemberVariable.value = false
    return showMemberVariable
  }
}

const mps = [
  { name: 'Albin Graf', party: 'USP (Conservative)' },
  { name: 'Edmund Sollis', party: 'USP (Conservative)' },
  { name: 'Gregor Vance', party: 'USP (Conservative)' },
  { name: 'Jon Velkar', party: 'USP (Reformist)' },
  { name: 'Klara Renik', party: 'USP (Reformist)' },
  { name: 'Armin Dorel', party: 'USP (Reformist)' },
  { name: 'Armin Pelik', party: 'PFJP (Democratic Socialist)' },
  { name: 'Ilya Kavel', party: 'PFJP (Democratic Socialist)' },
  { name: 'Dorin Selvek', party: 'PFJP (Democratic Socialist)' },
  { name: 'Johan Selm', party: 'NFP (Ethno-Nationalist)' },
  { name: 'Otto Velm', party: 'NFP (Ethno-Nationalist)' },
  { name: 'Karl Brenner', party: 'NFP (Ethno-Nationalist)' },
  { name: 'Faris Nadir', party: 'WPB (Ethnic Minority)' },
  { name: 'Zara Halim', party: 'WPB (Ethnic Minority)' },
  { name: 'Kemal Soran', party: 'WPB (Ethnic Minority)' },
]
</script>

<style scoped>
/* img {
} */
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.container2 {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.subContainer {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin: 15px;
}

.centerElement {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100vw;
}
.marginer {
  margin: 10px;
}

button {
  margin: 5px;
}
</style>
