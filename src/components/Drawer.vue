<script setup>
  import DrawerHead from "./DrawerHead.vue";
  import CartItem from "./CartItem.vue";
</script>

<template>
  <div class="fixed top-0 left-0 w-full h-full bg-black opacity-70"></div>
  <div class="bg-white w-96 h-full fixed top-0 right-0 z-20 p-8">
    <DrawerHead/>

    <CartItem/>
  </div>
</template>

<style scoped>

</style>