<template>
  <div>
    <nav
      id="header"
      class="w-full z-30 top-10 py-1 bg-main shadow-lg border-b border-main"
    >
      <div
        class="w-full flex items-center justify-between mt-0 px-6 py-2"
        @click="isOpen = !isOpen"
      >
        <label for="menu-toggle" class="cursor-pointer md:hidden block">
          <svg
            class="fill-current text-white"
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            viewBox="0 0 20 20"
          >
            <title>menu</title>
            <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"></path>
          </svg>
        </label>
        <input class="hidden" type="checkbox" id="menu-toggle" />

        <div
          class="hidden md:flex md:items-center md:w-auto w-full order-3 md:order-1"
          id="menu"
        >
          <nav>
            <ul
              class="md:flex items-center justify-between text-base text-blue-600 pt-4 md:pt-0"
            >
              <li>
                <a
                  class="inline-block no-underline hover:text-black text-white font-bold font-medium text-lg py-2 px-4 lg:-ml-2"
                  href="#"
                  >Home</a
                >
              </li>
              <li>
                <a
                  class="inline-block no-underline hover:text-black text-white font-bold font-medium text-lg py-2 px-4 lg:-ml-2"
                  href="#"
                  >Rails</a
                >
              </li>
              <li>
                <a
                  class="inline-block no-underline hover:text-black text-white font-bold font-medium text-lg py-2 px-4 lg:-ml-2"
                  href="#"
                  >Vue</a
                >
              </li>
              <li>
                <a
                  class="inline-block no-underline hover:text-black text-white font-bold font-medium text-lg py-2 px-4 lg:-ml-2"
                  href="#"
                  >React</a
                >
              </li>
            </ul>
          </nav>
        </div>

        <div
          class="order-2 md:order-3 flex flex-wrap items-center justify-end mr-0 md:mr-4"
          id="nav-content"
        ></div>
      </div>
    </nav>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      isOpen: false,
    }
  },
})
</script>

<style></style>
