<template>
  <div class="flex flex-col min-h-screen">
    <div class="flex-1 bg-sub pb-32">
      <slot />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'LayoutWrapper',
})
</script>

<style></style>
>
