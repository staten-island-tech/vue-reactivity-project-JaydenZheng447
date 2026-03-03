<template>
  <div class="container">
    <h1>Sordland 1954 Constitution</h1>
    <h3>
      USP (Conservative) Approval:
      <span>{{ USP_Conservative_love }}%</span>
    </h3>
    <h3>
      USP (Reformist) Approval: <span>{{ USP_Liberal_love }}%</span>
    </h3>
    <h3>
      NFP (Ethno-Nationalist) Approval: <span>{{ Nationalist_love }}%</span>
    </h3>
    <h3>
      PFJP (Western Liberalism) Approval: <span>{{ Democratic_Socialism_love }}%</span>
    </h3>
    <h3>
      WPB (Minority Rights) Approval: <span>{{ Ethnic_love }}%</span>
    </h3>
    <img @click="increment" src="" alt="" />
    <img @click="preview" src="" />
    <img: src="" />
    <h2>Amendment 1: The Supreme Court</h2>
    <p></p>
    <h2>Amendment 2: Term Limits</h2>
    <p>{{ s2 }}</p>
    <h2>Amendment 3: Cabinet Positions</h2>
    <p>{{ s3 }}</p>
    <h2>Amendment 4: Veto Limitations</h2>
    <p>{{ s4 }}</p>
    <button>&#8592</button>
    <button>&#8594</button>

  </div>

</template>

<script setup>
import { ref } from 'vue'

let USP_Conservative_love = ref(50)
let USP_Liberal_love = ref(50)
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

<!-- <style scoped>
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
</style> -->
