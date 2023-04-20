<template>
  <div>
    <h3>List Rendering</h3>
<div>
    <ul>
        <li v-for="(book ,index) of books" :key="book.id">
         <div>
          {{ book.title }}
         </div>
         <div>
          <input type="text">
         </div>
        </li>
    </ul>

    <div>
      <button @click="suffle">Click Me</button>
    </div>
    <ul>
      <li v-for="(value,key) in myObject">{{key}} - {{ value }}</li>
    </ul>
</div>
  </div>
  <template v-for="n in 5">
    <div>
      Raju Ponnamanda - {{ n }}
    </div>
    <div>Channel</div>
  </template>
</template>

<script setup lang="ts">
import {reactive,ref} from 'vue'
const parentMessage =ref('Book no.')
const books = reactive ([
{id:1, title: 'title 1'},
{id:2, title: 'title 2'},
{id:3, title: 'title 3'},
{id:4, title: 'title 4'},
{id:5, title: 'title 5'},
{id:6, title: 'title 6'},
{id:7, title: 'title 7'},
{id:8, title: 'title 8'},
{id:9, title: 'title 9'},
{id:10, title: 'title 10'},
 ]);

const myObject=reactive({

  title:'my title',
  author:'my author'
});
const suffle=()=>{
  books.sort(()=>Math.random()-0.5)
}
</script>

<style scoped></style>
4