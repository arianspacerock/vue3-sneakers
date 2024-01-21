<script setup>
 import { ref, onMounted} from "vue";
 import axios from "axios";

 const favorites = ref([])


 onMounted(async () => {
   try {
     const {data} = await axios.get('https://3740aa96c0805c9e.mokky.dev/favorites?_relations=items')

     favorites.value = data
   } catch (err) {
     console.log(err)
   }
 })
</script>

<template>
 <div>
   <h1>Избранное</h1>
 </div>
</template>

