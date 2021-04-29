<template>
  <layout-wrapper>
    <base-heading>ブログ詳細</base-heading>
    <img
      :src="thumbnail.url"
      alt="Thumbnail Image"
      class="rounded-t-xl object-cover w-full"
    />
    <p>{{ title }}</p>
    <p>{{ content }}</p>
    <span>{{ category && category.category_name }}</span>
    <p>{{ createdAt }}</p>
    <layout-button name="記事一覧に戻る" link="/blogs"></layout-button>
  </layout-wrapper>
</template>

<script lang="ts">
import Vue from 'vue'
import axios from 'axios'
import LayoutButton from '~/components/LayoutButton.vue'

export default Vue.extend({
  name: 'BlogDetail',
  components: { LayoutButton },
  // asyncDataサーバー側 && クライアント側で動作可能
  async asyncData({ params, $config }) {
    const { data } = await axios.get(`${$config.apiUrl}/blogs/${params.slug}`, {
      headers: { 'X-API-KEY': $config.apiKey },
    })
    return data
  },
})
</script>

<style></style>
