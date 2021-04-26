<template>
  <layout-wrapper>
    <div class="flex-1 bg-sub">
      <base-heading>ページ詳細</base-heading>
      <layout-button name="トップへ戻る" link="/" />
    </div>
  </layout-wrapper>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'BlogDetail',
})
</script>

<style>
.bg-sub {
  background-color: #edf2f7;
}
</style>