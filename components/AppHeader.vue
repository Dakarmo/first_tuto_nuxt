<template>
  <div>
   <nav class="mb-10 bg-gray-800  text-white p-4 shadow-md shadow-gray-900 flex item-center justify-between">
    <NuxtLink to="/" class="text-3xl font-bold">URLShortify</NuxtLink>

    <div class="space-x-3">
      <NuxtLink to="/me">Profile</NuxtLink>
      <NuxtLink to="/links">Liens</NuxtLink>
      <NuxtLink to="#">
        <Icon name="mdi:logout"/>
      </NuxtLink>
    </div>
   </nav>
  </div>
</template>

<script lang="ts" setup>


</script>
<style>

</style>