<script setup lang="ts">
definePageMeta({
  middleware: 'auth'
})

const userSession = useUserSession()
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
