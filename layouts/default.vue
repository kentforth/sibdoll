<script setup lang="ts">

</script>

<template>
<div>
  <header class="shadow-sm bg-white">
    <nav class="container mx-auto p-4 flex justify-between">
      <NuxtLink to="/">Home</NuxtLink>
      <ul>
        <li><NuxtLink to="/products" >Products</NuxtLink></li>
      </ul>
    </nav>
  </header>

  <div class="container mx-auto p-4">
    <slot />
  </div>
</div>
</template>

<style scoped>
.router-link-exact-active {
  color: orange;
}
</style>