<template>
  <div>
    <h2>Class Binding</h2>
    <div :class="{ active : isActive,'text-danger': hasError }">Apply Active Class</div>
  </div>
</template>

<script setup lang="ts">
import {ref} from'vue'
const isActive =ref(true)
const hasError =ref(true)

</script>

<style scoped></style>
