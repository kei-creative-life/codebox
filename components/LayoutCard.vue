<template>
  <div>
    <div class="flex justify-center">
      <div class="p-4">
        <div class="w-96 m-auto">
          <div
            class="grid grid-cols-3 grid-rows-7 grid-flow-row overflow-hidden rounded-lg shadow-md bg-white hover:shadow-xl transition-shadow duration-300 ease-in-out"
          >
            <div class="col-span-3 row-span-4 p-1 m-1">
              <a :href="link">
                <img
                  src="https://picsum.photos/640/400/?random"
                  alt="Placeholder"
                  class="rounded-t-xl object-cover h-48 w-full"
                />
              </a>
            </div>

            <div class="col-span-3 row-span-1">
              <header
                class="flex items-center justify-between leading-tight p-2 md:p-4"
              >
                <h1 class="text-lg">
                  <a class="no-underline hover:underline text-black" href="#">
                    {{ title }}
                  </a>
                </h1>
                <p class="text-grey-darker text-sm">{{ createdAt }}</p>
              </header>
            </div>

            <div class="col-span-3 row-span-1">
              <p>{{ content }}</p>
              <ul
                class="flex flex-row pl-2 text-gray-600 overflow-x-scroll hide-scroll-bar"
              >
                <li class="py-1">
                  <div
                    class="transition duration-300 ease-in-out rounded-2xl mr-1 px-2 py-1 hover:bg-blue-200 text-gray-500 hover:text-gray-800"
                  >
                    <a class="" href="#">#hogehoge</a>
                  </div>
                </li>
                <li class="py-1">
                  <div
                    class="transition duration-300 ease-in-out rounded-2xl mr-1 px-2 py-1 hover:bg-blue-200 text-gray-500 hover:text-gray-800"
                  >
                    <a class="" href="#">#fugafuga</a>
                  </div>
                </li>

                <li class="py-1">
                  <div
                    class="transition duration-300 ease-in-out rounded-2xl mr-1 px-2 py-1 hover:bg-blue-200 text-gray-500 hover:text-gray-800"
                  >
                    <a class="" href="#">#foofoo</a>
                  </div>
                </li>
                <li class="py-1">
                  <div
                    class="transition duration-300 ease-in-out rounded-2xl mr-1 px-2 py-1 hover:bg-blue-200 text-gray-500 hover:text-gray-800"
                  >
                    <a class="" href="#">#barbarbar</a>
                  </div>
                </li>
                <li class="py-1">
                  <div
                    class="transition duration-300 ease-in-out rounded-2xl mr-1 px-2 py-1 hover:bg-blue-200 text-gray-500 hover:text-gray-800"
                  >
                    <a class="" href="#">#hogefugafoo</a>
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
  name: 'layoutCard',
  props: {
    link: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    content: {
      type: String,
      required: true,
    },
    createdAt: {
      type: Date,
    },
  },
})
</script>

<style></style>
