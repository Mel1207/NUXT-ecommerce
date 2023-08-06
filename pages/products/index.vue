<template>
  <h3>index products</h3>
  <div class="grid grid-cols-4 gap-5">
    <div v-for="p in products">
      <ProductCard :product="p"/>
    </div>
  </div>
</template>

<script setup>
  definePageMeta({
    layout: 'products-layout'
  })

  // FETCH PRODUCTS VIA API
  const { data: products } = await useFetch('https://fakestoreapi.com/products')

  // CUSTOM META DATA
  useHead({
    title: 'NUXT Merch | Products',
    meta: [{
      name: 'description', 
      content: 'Merch inside NUXT'
    }]
  })
</script>