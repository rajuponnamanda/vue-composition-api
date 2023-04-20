<template>
    <div>
<h3>Form Input</h3>
<div>
    <input type="text" :value="text" @input="(event )=> ( text = event.target.value )">
</div>
<div>
    <input type="text" v-model="message">
</div>
<input type="checkbox" value="ram " v-model="checkedNames">
<input type="checkbox" value="rakshith" v-model="checkedNames">
<input type="checkbox" value="Ponnamanda" v-model="checkedNames">
{{ checkedNames }}
<p>{{ message }}</p>
<p>{{ text }}</p>


<div>
    <input type="radio" value="one" v-model="picked">
    <input type="radio" value="twooo" v-model="picked">
</div>
<div>{{ picked }}</div>


<div>Selected Value : {{ selected }}</div>
<select v-model="selected">
<option>A</option>
<option>B</option>
<option>C</option>
<option>D</option>
</select>
   </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'

const text =ref('emaipoyavey')
const message=ref("elavunnav raaa")
const checked=ref(true)
const  checkedNames=ref([])
const picked =ref()
const selected=ref('A')
</script>

<style scoped>

</style>