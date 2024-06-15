<template>
  <div class="prose">
    <h1>Inscription</h1>
    <form>
      <label >
        Nom et prénom
        <input type="text">
      </label>
      <label >
        Email
        <input type="email">
      </label>
      <label >
        Mot de passe
        <input type="password">
      </label>
      <label >
        Confirmation Mot de passe
        <input type="password">
      </label>
      <button  class="btn">S'inscrire</button>
    </form>
    <p>Vous avez déjà un compte ?
      <NuxtLink to="/login" class = "underline text-blue-400">Inscrivez-vous !</NuxtLink>
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