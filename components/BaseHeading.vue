<template>
  <h2 class="font-sans text-2xl font-bold mt-10 text-grey-800 text-center">
    <slot />
  </h2>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'BaseHeading',
})
</script>

<style scoped>
</style>