<template>
  <layout-wrapper>
    <base-heading>ブログ一覧</base-heading>
    <div class="flex justify-center flex-wrap">
      <layout-card
        v-for="(blog, index) in blogs"
        :id="blog.id"
        :key="index"
        :title="blog.title"
        :content="blog.content"
        :thumbnail="blog.thumbnail && blog.thumbnail.url"
        :category="blog.category && blog.category.category_name"
        :createdAt="blog.createdAt"
      />
    </div>
    <div class="mt-5">
      <layout-button name="トップへ戻る" link="/" />
    </div>
    <pagination></pagination>
  </layout-wrapper>
</template>

<script lang="ts">
import Vue from 'vue'
import axios from 'axios'

export default Vue.extend({
  name: 'Blogs',
  async asyncData({ params, $config }) {
    const page = params.p || '1'
    const limit = 3
    const { data } = await axios.get(
      `${$config.apiUrl}/blogs?limit=${limit}&offset=${
        (Number(page) - 1) * limit
      }`,
      {
        headers: { 'X-API-KEY': $config.apiKey },
      }
    )
    return {
      blogs: data.contents,
    }
  },
})
</script>

<style></style>
