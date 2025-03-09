<script setup lang="ts">
definePageMeta({
  middleware: 'auth'
})
</script>

<template>
<section>
  <h1>User Page</h1>
  <p>
    <nuxt-link to="/">Home</nuxt-link>
  </p>
</section>
</template>

<style scoped>

</style>
