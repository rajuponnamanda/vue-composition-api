<template>
  <div>
    <div>
      <h1 :style="[baseStyle, baseStyle2]">Computed Property</h1>
      <p>Employees Presents: {{ isEmployeesPresent }}</p>
      <p>Full Name: {{ fullName }}</p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { computed, reactive, ref } from 'vue'
const employees = reactive(['emp1', 'emp2'])

const firstName = ref('Raju')
const lastName = ref('Ponnamanda')

const isEmployeesPresent = computed(() => {
  return employees.length ? 'Yes Computed' : 'No'
})
const fullName = computed(() => {
  return firstName.value + '' + lastName.value
})
const baseStyle = reactive({
  color: 'red',
  fontSize: '20px'
})
const baseStyle2 = reactive({
  border: '2px solid red',
  color: 'green',
  width: 'auto'
})
</script>

<style scoped></style>
