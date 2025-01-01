<script setup lang="ts">
useHead({
  title: 'Products',
})

const { data: products } = await useFetch('https://fakestoreapi.com/products')


</script>

<template>
<div>
  Products
 <div>
   <div class="grid grid-cols-4 gap-5">
     <div v-for="product in products" :key="product.id">
        <NuxtLink :to="{ name: 'products-id', params: { id: product.id } }">{{product.title}}</NuxtLink>
     </div>
   </div>
 </div>
</div>
</template>

<style scoped>

</style>