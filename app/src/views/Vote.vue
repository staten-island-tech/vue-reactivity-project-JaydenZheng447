<template>
  <div class="container2">
    <span class="approvalBar">
      Conservative Approval:
      <span>{{ Conservative_love }}%</span>
    </span>
    <span class="approvalBar">
      Reformist Approval: <span>{{ Liberal_love }}%</span>
    </span>
    <span class="approvalBar">
      Ethno-Nationalist Approval: <span>{{ Nationalist_love }}%</span>
    </span>
    <span class="approvalBar">
      Democratic Socialist Approval: <span>{{ Democratic_Socialism_love }}%</span>
    </span>
    <span>
      Ethnic Minority Approval: <span>{{ Ethnic_love }}%</span>
    </span></div>
  <div class="container">
    <h1 class="marginer">Sordland 1954 Constitution</h1>
    <img @click="increment" src="" alt="" />
    <img @click="preview" src="" />
    <img: src="" />
        <h1 class = "marginer">Amendments</h1>
    <h2>Amendment 1: The Supreme Court</h2>
    <p></p>
      
    <h2>Amendment 2: Term Limits</h2>
    <div class="subContainer">
          <button>&#8592</button><p>{{ s2 }}</p>
    <button>&#8594</button>
    </div>
    <h2>Amendment 3: Cabinet Positions</h2>
    <div class="subContainer">
          <button>&#8592</button><p>{{ s3 }}</p>
    <button>&#8594</button>
  </div>
        
    <h2>Amendment 4: Veto Limitations</h2>
<div class="subContainer">
    <button>&#8592</button>  <p>{{ s4 }}</p>
    <button>&#8594</button>
     </div>
      <RouterLink to="/test-view">Test Views</RouterLink>
  </div>

</template>

<script setup>
import { ref } from 'vue'

let Conservative_love = ref(50)
let Liberal_love = ref(50)
let Nationalist_love = ref(50)
let Democratic_Socialism_love = ref(50)
let Ethnic_love = ref(50)
let Current_arrow = ref(1)
let s1 = ""
let s2 = ""
let s3 = ""
let s4 = ""
s2 = s2a
s3 = s3a
s4 = s4a
const s2a = "No term limits"
const s2b = "Two-term limit"
const s3a = "Cabinet members are appointed by the President at will"
const s3b = "Cabinet members are appointed by the President from an approved list presented by Parliament"
const s3c = "Cabinet members are appointed by Parliament"
const s4a = "The President may veto any bill"
const s4b = "Presidential vetoes can be overturned by a 2/3rd majority in Parliament"
const s4c = "The Presidential veto shall be abolished"

function increment() {
  count.value -= 5
}
const SnowArray = ref(['1'])
console.log(SnowArray)
function preview() {}
</script>

<style scoped>
img {
}
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 40vh;
  max-width: 20vw;
}
.container2 {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  height: 40vh;
}

.subContainer {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}
.marginer{
  margin: 10px;
}
.approvalBar{
  border: 10px;
  border-color: black;
  margin: 10px;
color:blue;
min-width: 15 vw;
}

button{
  margin:5px;
}
</style>
