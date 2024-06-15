<template>
  <div class="prose">
    <h1>Connexion</h1>
    <form>
      <label >
        Email
        <input type="email">
      </label>
      <label >
        Mot de passe
        <input type="password">
      </label>
      <button  class="btn">Se Connecter</button>
    </form>
    <p>Pas de compte ?
      <NuxtLink to="/register" class = "underline text-blue-400">Inscrivez-vous !</NuxtLink>
    </p>
  </div>
</template>

<script lang="ts" setup>
  definePageMeta({
    layout: 'centered'
  })
</script>

<style>

</style>