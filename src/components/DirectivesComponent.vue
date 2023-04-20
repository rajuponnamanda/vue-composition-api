<template>
  <div>
    <h3>Conditional Rendering</h3>
    <div>
      <button @click="isAwsome = !isAwsome">Toggle</button>
    </div>
    <div v-if="isAwsome">Vue is Awsome</div>
    <div v-else="!isAwsome">Oh No It!! Is Not Awsome...</div>
    <div v-show ="isAwsome">is Akndksnfks </div>
    <div v-if="type === 1">1</div>
    <div v-if="type === 2">2</div>
    <div v-if="type === 3">3</div>
    <div v-if="type === 4">4</div>
    <div v-if="type === 5">5</div>
    <div v-if="type === 6">6</div>
    <div v-if="type === 7">7</div>
    <div v-if="type === 8">8</div>
    <div v-if="type === 9">9</div>
    <div v-if="type === 10">10</div>
    <div v-if="type === 11">11</div>
    <div v-if="type === 12">12</div>
    <div v-else-if="type">Not a Number</div>

    <div v-if="showPara">
    <h4>Paragraph</h4>
    <p>
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo vitae aspernatur dolore
      recusandae laudantium numquam harum atque, quod debitis placeat. Ea voluptatum, sunt saepe ad
      a pariatur quas iure voluptates.
    </p>
    <p>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nihil maiores minus at? Ipsum
      maiores facilis perspiciatis reprehenderit? A autem veniam laborum voluptates. Minima ratione
      eius aut eos, et voluptas! A.
    </p>
</div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const isAwsome = ref(true)
const type = ref(1)
setInterval(() => {
  type.value++
}, 1000)
const showPara = ref(true)
</script>

<style scoped></style>
