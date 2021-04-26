<template>
  <layout-wrapper>
    <base-heading>ブログ一覧</base-heading>
    <layout-card
      link="/blog-detail"
      v-for="(blog, index) in blogs"
      :key="index"
      :title="blog.title"
      :content="blog.content"
      :createdAt="blog.createdAt"
    />
    <layout-button name="トップへ戻る" link="/" />
  </layout-wrapper>
</template>

<script lang="ts">
import Vue from 'vue'
import axios from 'axios'

export default Vue.extend({
  name: 'Blogs',
  async asyncData({ $config }) {
    const { data } = await axios.get(`${$config.apiUrl}/blogs`, {
      headers: { 'X-API-KEY': $config.apiKey },
    })
    return {
      blogs: data.contents,
    }
  },
})
</script>

<style></style>
