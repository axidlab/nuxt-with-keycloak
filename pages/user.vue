<script setup lang="ts">
const userSession = useUserSession()

definePageMeta({
  middleware: 'auth'
})
</script>

<template>
<section>
  <h1>User Page</h1>
  <div>
    {{ userSession }}
  </div>
  <p>
    <nuxt-link to="/">Home</nuxt-link>
  </p>
</section>
</template>

<style scoped>

</style>
