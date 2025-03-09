<script setup>
const { loggedIn, user, session, fetch, clear, openInPopup } = useUserSession()
</script>

<template>
  <div>
    <div v-if="loggedIn">
      <h1>Hello {{ user.login }}!</h1>
      <p>Logged in since {{ session.loggedInAt }}</p>
      <!-- TODO: call keycloak to logout -->
      <!-- https://idm.test.axidflow.eu/realms/axs/protocol/openid-connect/logout -->
      <button @click="clear">Logout</button>
    </div>
    <div v-else>
      <h3>Not logged in</h3>
      <a href="/api/auth/keycloak">Login with Keycloak...</a>
      <button @click="openInPopup('/api/auth/keycloak')">Login with Keycloak</button>
    </div>
    <hr />
    <NuxtPage />
  </div>
</template>
