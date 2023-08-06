<template>
  <div>
    <header class="shadow-sm bg-white">
      <nav class="container mx-auto p-4 flex justify-between">
        <NuxtLink to="/" class="font-bold">Ecom</NuxtLink>
        <ul class="flex gap-4">
          <li>
            <NuxtLink to="/">Home</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/about">About</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/products" class="btn text-white">Products</NuxtLink>
          </li>
        </ul>
      </nav>

      <!-- output the page content -->
      <div class="container mx-auto p-4">
        <slot/>
      </div>
    </header>
  </div>
</template>

<script>
export default {
 
}
</script>

<style scoped>
.router-link-exact-active{
  color: #12b488;
}
</style>