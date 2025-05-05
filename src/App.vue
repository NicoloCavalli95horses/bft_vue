<template>
  <Thumbnail v-for="item in items" :key="item.id" :item='item' />
</template>

<script setup>
//=============
// Import
//=============
import Thumbnail from './components/Thumbnail.vue';

//=============
// Consts
//=============
const items = [
  {id: 1, is_premium: false, src:"https://picsum.photos/id/10/200/300"},
  {id: 2, is_premium: true,  src:"https://picsum.photos/id/20/200/300"},
  {id: 3, is_premium: true,  src:"https://picsum.photos/id/30/200/300"},
  {id: 4, is_premium: false, src:"https://picsum.photos/id/40/200/300"},
  {id: 5, is_premium: false, src:"https://picsum.photos/id/50/200/300"},
  {id: 6, is_premium: true,  src:"https://picsum.photos/id/60/200/300"}
];

</script>

<style scoped>
</style>
