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
const items = await getData();


//=============
// Functions
//=============
async function getData() {
  const url = 'https://nestjs-server-0011.onrender.com/images';
  try {
    const response = await fetch(url);
    if (!response.ok) {
      throw new Error(`Response status: ${response.status}`);
    }

    return await response.json();
  } catch (error) {
    console.error(error.message);
  }
}

</script>

<style scoped></style>
