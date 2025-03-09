<script setup>
const { loggedIn, user, session, clear  } = useUserSession()

watch(loggedIn, () => {
  if (!loggedIn.value) {
    navigateTo('/')
  }
})
</script>

<template>
  <div>
    <div v-if="loggedIn">
      <h1>Hello {{ user.name }} (<a :href="'mailto:' + user.email">{{ user.email }}</a>)!</h1>
      <p>Logged in since {{ session.loggedInAt }}</p>
      <button @click="clear">Logout</button>
    </div>
    <div v-else>
      <h3>Not logged in</h3>
      <a href="/api/auth/keycloak">Login with Keycloak...</a>
    </div>
    <hr />
    <NuxtPage />
  </div>
</template>
