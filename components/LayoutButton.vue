<template>
  <div class="text-center">
    <button
      type="button"
      class="bg-main text-white px-3 py-2 rounded-md font-bold"
    >
      <a :href="link"> {{ name }}</a>
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

<style>
.bg-main {
  background-color: #139299;
}
</style>