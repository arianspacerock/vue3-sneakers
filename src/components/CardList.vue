<script setup>
import Card from "./Card.vue";

defineProps({
  items: Array
})

const emit = defineEmits(['addToFavorite'])

</script>

<template>
  <div class="grid grid-cols-4 gap-5">
    <Card
          v-for="item in items"
          :key="item.id"
          :title="item.title"
          :imageUrl="item.imageUrl"
          :price="item.price"
          :isFavorite="item.isFavorite"
          :id="item.id"
          :onClickFavorite="() =>emit('addToFavorite', item)"
          :onClickAdd="onClickAdd"
    />
  </div>
</template>

