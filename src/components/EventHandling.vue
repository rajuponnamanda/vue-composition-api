<template>
    <div>
<div>
    <h3>Event Handling</h3>
    <div>
        <button v-on:click="count++">Counter</button>
        <p>Counter : {{ count }}</p>
    </div>
</div>
    </div>
</template>

<script setup lang="ts">
import {ref} from 'vue'
const count= ref(0);
</script>

<style scoped>

</style>