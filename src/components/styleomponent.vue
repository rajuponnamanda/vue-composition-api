<template>
    <div>
<h1>Style Binding</h1>
<div :style="styleObject">Applying Styles</div>
    </div>
</template>

<script setup lang="ts">
import { computed } from '@vue/reactivity';
import {ref,reactive} from 'vue'
const activeColor =ref('red');
const fontSize =ref(30)
const fontFamily=ref("Lucida Console")

const styleObject =computed(()=>{
    return{
    color: activeColor.value,
    fontSize: fontSize.value + 'px',
    fontFamily: fontFamily.value
}
});

setTimeout(()=>{
 console.log('fired');
 activeColor.value = 'blue',
 fontSize.value=50;

 },5000);
</script>

<style scoped>

</style>