<template>
  <div class="mt-7 max-w-sm mx-auto text-center">
    <p class="mt-7 text-7xl font-bold">{{ error.statusCode }}</p>
    <p class="mt-7 text-6xl" >Oops.</p>
    <p class="mt-7">{{ error.message }}</p>
    <button class="btn my-7 text-white bg-slate-400 p-4" @click="handleClearError">Go Home...</button>
  </div>
</template>

<script setup>
  defineProps(['error'])
  const handleClearError = () => {
    clearError({ redirect: '/'})
  }

</script>

<style scoped>

</style>