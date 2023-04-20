<template>
    <div>
<h3>Watch Property</h3>
<div>
    <p>Ask Yes/No Questions ?</p>
    <input type="text" v-model="question">
</div>
<div>Answer : {{ answer }}</div>
<img :src="responseData.image" style="width:150px"/>
    </div>
</template>

<script setup lang="ts">
import {ref, watch} from 'vue';

const question =ref('');
const answer =ref('Questipon generally contain ?');
const responseData = ref('')

watch(question, async (newQuestion, oldQuestion) =>{
if(newQuestion.indexOf('?')>-1){
    answer.value = 'Thinking.....';
    responseData.value ='';

    try{
        const res =await fetch('https://yesno.wtf/api');
        const resJson =await res.json();
        answer.value = resJson.answer;
    } catch(error){
        answer.value ='Error!. Could Not reach the api'
    }
}
});
</script>

<style scoped>

</style>