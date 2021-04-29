<template>
  <div>
    <div class="flex justify-center">
      <div class="p-4">
        <div class="w-96 m-auto">
          <div
            class="grid grid-cols-3 grid-rows-7 grid-flow-row overflow-hidden rounded-lg shadow-md bg-white hover:shadow-xl transition-shadow duration-300 ease-in-out"
          >
            <div class="col-span-3 row-span-4 p-1 m-1">
              <nuxt-link :to="`/${id}`">
                <img
                  :src="thumbnail"
                  alt="Thumbnail Image"
                  class="rounded-t-xl object-cover h-48 w-full"
                />
              </nuxt-link>
            </div>

            <div class="col-span-3 row-span-1">
              <header
                class="flex items-center justify-between leading-tight p-2 md:p-4"
              >
                <h1 class="text-lg">
                  <nuxt-link :to="`/${id}`">
                    {{ title }}
                  </nuxt-link>
                </h1>
              </header>
              <h2 class="px-2 pb-2 md:px-4 pb-2">{{ content }}</h2>
            </div>

            <div class="col-span-3 row-span-1">
              <ul
                class="flex flex-row pl-2 text-gray-600 overflow-x-scroll hide-scroll-bar"
              >
                <li class="py-1">
                  <div
                    class="transition duration-300 ease-in-out rounded-2xl mr-1 px-2 py-1 hover:bg-blue-200 text-sub hover:text-gray-800"
                  >
                    <a class="" href="#"
                      ><span class="pr-1">#</span
                      >{{ category ? category : 'Home' }}</a
                    >
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'LayoutCard',
  props: {
    id: {
      type: String,
      default: '',
    },
    title: {
      type: String,
      default: '',
    },
    content: {
      type: String,
      default: '',
    },
    thumbnail: {
      type: String,
      default: 'https://picsum.photos/640/400/?random',
    },
    category: {
      type: String,
      default: 'none',
    },
    createdAt: {
      type: String,
      default: '',
    },
  },
})
</script>

<style></style>
