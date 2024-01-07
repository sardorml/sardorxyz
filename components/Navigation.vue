<template>
  <div
    class="nav shadow-one blur-none opacity-95 transition ease-in-out duration-300 delay-100 z-30"
  >
    <div class="flex nav-content justify-between">
      <div class="pl-8 lg:pl-0">
        <nuxt-link to="#" class="text-3xl text-white font-medium"
          ><span class="blinker text-teal-300 font-light">_</span>sardor<span
            class="text-teal-300 font-light"
            >.xyz</span
          ></nuxt-link
        >
      </div>
      <div class="items-center text-sm font-light hidden lg:flex">
        <nuxt-link class="text-gray-300 pl-8" to="#about">About</nuxt-link>
        <nuxt-link class="text-gray-300 pl-8" to="#skills">Skills</nuxt-link>
        <nuxt-link class="text-gray-300 pl-8" to="#experience"
          >Experience</nuxt-link
        >
        <nuxt-link class="text-gray-300 pl-8" to="#contact">Contact</nuxt-link>

        <div class="relative ml-8">
          <div class="bg-[#64ffda] absolute inset-0 rounded-md"></div>
          <a href="/path/to/resume.pdf" download class="relative">
            <button
              class="border border-[#64ffda] text-[#64ffda] font-light p-2 rounded-md text-sm transition ease-in duration-150 hover:-translate-x-1 hover:-translate-y-1 bg-[#0a192f]"
            >
              Resume
            </button>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.nav {
  width: 100%;
  position: fixed;
  margin-bottom: unset;
  background: #0a192f;
  /* border-bottom: 0.01em solid rgb(204, 204, 204); */
}
.nav-content {
  max-width: 1280px;
  margin: 0px auto;
  padding: 1.4rem 0px;
}
.blinker {
  animation: blinker 1s linear infinite;
}

@keyframes blinker {
  50% {
    opacity: 0;
  }
}
</style>
