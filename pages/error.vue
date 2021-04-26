<template>
  <layout-wrapper>
    <div class="flex-1 bg-sub">
      <div class="container w-full mx-auto">
        <div class="mb-20">
          <p class="text-center text-2xl font-medium text-grey-900 font-bold">
            ページが見つかりません
          </p>
        </div>
        <layout-button name="トップページに戻る" link="/"></layout-button>
      </div>
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

<style>
.text-main {
  color: #139299;
}
.border-main {
  border-color: #139299;
}
.bg-main {
  background-color: #139299;
}
.bg-sub {
  background-color: #edf2f7;
}
</style>
