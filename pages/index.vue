<template>
  <layout-wrapper>
    <div class="flex-1 bg-sub">
      <base-heading>おすすめ記事</base-heading>
      <layout-card />
      <layout-button name="記事一覧" link="/blogs" />
    </div>
  </layout-wrapper>
</template>

<script lang="ts">
import Vue from 'vue'
import BaseHeading from '~/components/BaseHeading.vue'

export default Vue.extend({
  components: { BaseHeading },
})
</script>

<style></style>
