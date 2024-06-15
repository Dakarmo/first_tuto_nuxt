<template>
  <div class="relative">
    <Icon name="mdi:magnify" class="absolute w-6 h-6 top-[50%] translate-y-[-50%]"/>
    <input 
      type="text" 
      placeholder="Rechercher un lien" 
      class="pl-10 inline-block"
      v-model="modelValue"
    >
    <!-- <p>{{ modelValue }}</p> -->
  </div>
</template>

<script lang="ts" setup>

  // defineProps({
  //   modelValue: {type: String, require: true}
  // })

//  const props = defineProps<{
//     modelValue: string;
//   }>();

const modelValue = defineModel()

</script>

<style>


</style>