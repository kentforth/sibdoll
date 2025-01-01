<script setup lang="ts">
const { id } = useRoute().params

const uri = 'https://fakestoreapi.com/products/' + id

console.log('URI', uri)

const {data: product} = await useFetch(uri)

if (!product.id) {
  throw createError({statusCode: 404, statusMessage: 'Not Found'})
}
</script>

<template>
<div>
  Product details for {{ id }}
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Beatae cumque et harum id iusto laborum nulla praesentium quisquam tempore vel!</p>
</div>
</template>

<style scoped>

</style>