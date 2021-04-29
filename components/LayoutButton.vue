<template>
  <div class="text-center">
    <button
      type="button"
      class="text-sm md:text-base bg-main text-white px-6 py-4 rounded-md font-bold"
    >
      <nuxt-link :to="link">{{ name }}</nuxt-link>
    </button>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'LayoutButton',
  props: {
    name: {
      type: String,
      required: true,
    },
    link: {
      type: String,
      required: true,
    },
  },
})
</script>

<style></style>
