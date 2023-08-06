<template>
  <div>
    <Head>
      <Title>NUXT ECOM | {{ product.title }}</Title>
      <Meta name="description" :content="product.description" />
    </Head>
    <ProductDetails :product="product"/>
  </div>
</template>

<script setup>
  definePageMeta({
    layout: 'products-layout'
  })
  const { id } = useRoute().params

  const url = 'https://fakestoreapi.com/products/' + id

  // FETCH THE PRODUCT
  const { data: product } = await useFetch(url, {key: id})
  if(!product.value) {
    throw createError({
      statusCode: 404,
      statusMessage: 'Product Not Found!',
      fatal: true
    })
  }


</script>