<template>
<div class="counting">
<h1>Counting</h1>

<button @click="increaseCounter()">Increse</button>
<span>{{counter}}</span>
<button @click="decreaseCounter()">Decrease</button>
<h4>Counter Vsalue {{ evenOrOdd }}</h4>
<div v-html="message"></div>

<computedVue/>
<ClassComponentVue/>
<styleomponent/>
<DirectivesComponent/>
<ListRendering/>
<EventHandling/>
<FormInput/>
<WatchComponent/>
<div style="margin-top:15rem"></div>
  </div>
</template> 

<script setup lang="ts">
import computedVue from './components/compuited.vue'
import ClassComponentVue from './components/ClassComponent.vue'
import styleomponent from './components/styleomponent.vue';
import DirectivesComponent from './components/DirectivesComponent.vue';
import ListRendering from './components/ListRendering.vue';
import EventHandling from './components/EventHandling.vue';
import FormInput from './components/FormInput.vue';
import WatchComponent from './components/WatchComponent.vue';
 
import {ref,computed} from "vue"
let counter = ref<number>(0)

const evenOrOdd = computed(() => {
return counter.value %2 ===0 ? 'Even':'Odd'

});

const increaseCounter=()=>{
  counter.value++
 
}
const decreaseCounter=()=>{
  counter.value--
}
const message='<h1>Hello Every One</h1>'
</script>

<style scoped>
.counting{
  text-align: center;
  margin-top: 10%;
}
span{
  margin: 10px;
}
</style>