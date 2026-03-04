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
    </span>
  </div>
  <div class="container">
    <h1 class="marginer">Sordland 1954 Constitution</h1>
    <img @click="increment" src="" alt="" />
    <img @click="preview" src="" />
    <img: src="" />
    <h1 class="marginer">Amendments</h1>
    <h2>Amendment 1: The Supreme Court</h2>
    <p></p>

    <h2>Amendment 2: Term Limits</h2>
    <div class="subContainer">
      <button @click="s2_arrow('left')">&#8592;</button>
      <p>{{ s2 }}</p>
      <button @click="s2_arrow('right')">&#8594;</button>
    </div>
    ''
    <h2>Amendment 3: Cabinet Positions</h2>
    <div class="subContainer">
      <button>&#8592;</button>
      <p>{{ s3 }}</p>
      <button>&#8594;</button>
    </div>

    <h2>Amendment 4: Veto Limitations</h2>
    <div class="subContainer">
      <button>&#8592;</button>
      <p>{{ s4 }}</p>
      <button>&#8594;</button>
    </div>
    <RouterLink to="/test-view">Test Views</RouterLink>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { reactive } from 'vue'

let Conservative_love = ref(50)
let Liberal_love = ref(50)
let Nationalist_love = ref(50)
let Democratic_Socialism_love = ref(50)
let Ethnic_love = ref(50)
let Current_arrow = ref(1)

let s1_val = 0
let s2_val = 0
let s3_val = 0
let s4_val = 0

let s2_array = ['No term limits', 'Two-term limit']
let s3_array = [
  'Cabinet members are appointed by the President at will',
  'Cabinet members are appointed by the President from an approved list presented by Parliament',
  'Cabinet members are appointed by Parliament',
]
let s4_array = [
  'The President may veto any bill',
  'Presidential vetoes can be overturned by a 2/3rd majority in Parliament',
  'The Presidential veto shall be abolished',
]

let s1 = ''
let s2 = s2_array[s2_val]
let s3 = s3_array[s3_val]
let s4 = s4_array[s4_val]

function s2_arrow(input) {
  console.log(input)
  if (input === 'left') {
    if (s2_val > 0) {
      s2_val -= 1
      s2 = s2_array[s2_val]
    } else {
      console.log('Desired value out of range')
    }
  } else if (input === 'right') {
    if (s2_val < s2_array.size) {
      s2_val += 1
      s2 = s2_array[s2_val]
    } else {
      console.log('Desired value out of range')
    }
  } else {
    s2 = 'An unexpected error has occured'
    console.log('An unexpected error has occured on Amendment 2')
  }
}

function s3_arrow(input) {
  if (input === 'left') {
    if (s3_val > 0) {
      s3_val -= 1
      s3 = s3_array[s3_val]
    } else {
      console.log('Desired value out of range')
    }
  } else if (input === 'right') {
    if (s3_val < s3_array.size) {
      s3_val += 1
      s3 = s3_array[s3_val]
    } else {
      console.log('Desired value out of range')
    }
  } else {
    s3 = 'An unexpected error has occured'
    console.log('An unexpected error has occured on Amendment 3')
  }
}

function s4_arrow(input) {
  if (input === 'left') {
    if (s4_val > 0) {
      s4_val -= 1
      s4 = s4_array[s4_val]
    } else {
      console.log('Desired value out of range')
    }
  } else if (input === 'right') {
    if (s4_val < s4_array.size) {
      s4_val += 1
      s4 = s4_array[s4_val]
    } else {
      console.log('Desired value out of range')
    }
  } else {
    s4 = 'An unexpected error has occured'
    console.log('An unexpected error has occured on Amendment 2')
  }
}

/* 
function s2_arrow(input) {
  if (input === 'left') {
    if (s2_val > 0) {
      s2_val.value--
      s2 = s2_array[s2_val]
    } else {
      console.log('Desired value out of range')
    }
  } else if (input === 'right') {
    if (s2_val < s2_array.size) {
      s2_val.value++
      s2 = s2_array[s2_val]
    } else {
      console.log('Desired value out of range')
    }
  } else {
    s2 = 'An unexpected error has occured'
    console.log('An unexpected error has occured on Amendment 2')
  }
}

function s3_arrow(input) {
  if (input === 'left') {
    if (s3_val > 0) {
      s3_val.value--
      s3 = s3_array[s3_val]
    } else {
      console.log('Desired value out of range')
    }
  } else if (input === 'right') {
    if (s3_val < s3_array.size) {
      s3_val.value++
      s3 = s3_array[s3_val]
    } else {
      console.log('Desired value out of range')
    }
  } else {
    s3 = 'An unexpected error has occured'
    console.log('An unexpected error has occured on Amendment 3')
  }
}

function s4_arrow(input) {
  if (input === 'left') {
    if (s4_val > 0) {
      s4_val.value--
      s4 = s4_array[s4_val]
    } else {
      console.log('Desired value out of range')
    }
  } else if (input === 'right') {
    if (s4_val < s4_array.size) {
      s4_val.value++
      s4 = s4_array[s4_val]
    } else {
      console.log('Desired value out of range')
    }
  } else {
    s4 = 'An unexpected error has occured'
    console.log('An unexpected error has occured on Amendment 2')
  }
} */

function increment() {
  count.value -= 5
}
const SnowArray = ref(['1'])
console.log(SnowArray)
function preview() {}
</script>

<style scoped>
/* img {
} */
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 40vh;
  /* max-width: 20vw; */
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
.marginer {
  margin: 10px;
}
.approvalBar {
  border: 10px;
  border-color: black;
  margin: 10px;
  color: blue;
  min-width: 15 vw;
}

button {
  margin: 5px;
}
</style>
