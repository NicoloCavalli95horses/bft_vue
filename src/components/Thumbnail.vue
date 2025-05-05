<template>
    <div class="img-wrapper" @click="onClick">
        <img :src="item.src" :alt="item.alt || 'img'">
        <div v-if="item.is_premium" class="badge">🔒</div>
    </div>
</template>

<script setup>
//=============
// Props
//=============
const props = defineProps({
  item: {
    type: Object,
    default: () => ({})
  }
});


//=============
// Functions
//=============
function onClick() {
  alert(props.item.is_premium ? 'premium content' : 'free content');
}

</script>

<style scoped>

.img-wrapper {
  margin: 10px;
  position: relative;
  cursor: pointer;
}

.badge {
  position: absolute;
  bottom: 10px;
  right: 6px;
  border-radius: 4px;
  background-color: lightyellow;
  font-size: 20px;
}

</style>