<template>
  <div class="hero pb-48">
    <div class="grid grid-cols-3">
      <!-- Text -->
      <div class="col-span-3 lg:col-span-2">
        <h1
          v-motion-slide-visible-top
          class="md:text-7xl text-5xl text-slate-200"
        >
          Hi, my <br />
          name is <b>Sardor</b>
        </h1>
        <p
          v-motion-fade-visible
          class="md:text-xl text-xl text-slate-400 mt-8 md:leading-relaxed"
        >
          I have 6+ years of experience developing and launching web<br />
          and mobile applications using
          <span class="text-teal-300">VueJS</span>,
          <span class="text-teal-300">React</span>,
          <span class="text-teal-300">React Native</span>,
          <span class="text-teal-300">TypeScript</span>,<br />
          <span class="text-teal-300">Node.js</span>, and
          <span class="text-teal-300">Firebase</span>. Led the development of
          several web applications used by ranging from 10,000 - 1,000,000+
          users.
        </p>
        <div v-motion-slide-visible-bottom class="relative w-fit mt-8">
          <div class="bg-[#64ffda] absolute inset-0 rounded-md"></div>
          <a
            href="/cv_sardor_2024.pdf"
            download
            class="relative"
            target="_blank"
          >
            <button
              class="border border-[#64ffda] text-[#64ffda] font-sm py-4 px-3 rounded-md text-md transition ease-in duration-150 hover:-translate-x-1 hover:-translate-y-1 bg-[#0a192f]"
            >
              Download Resume
            </button>
          </a>
        </div>
      </div>
      <!-- Image -->
      <div
        v-motion-slide-visible-right
        class="hidden lg:block lg:ml-28 flex flex-col col-span-3 md:col-span-1 cursor-pointer lg:mx-6"
      >
        <div class="relative">
          <div
            class="absolute inset-0 rounded-md border border-[#64ffda]"
          ></div>
          <div
            class="bg-white rounded-md p-6 transition ease-in duration-150 hover:-translate-x-3 hover:-translate-y-3 h-full -translate-y-2 -translate-x-2"
          >
            <div class="rounded-full relative overflow-hidden">
              <img
                src="/images/hero/portrait2.jpeg"
                alt="Hero Image"
                style="object-fit: contain"
                class="w-full h-full"
              />
            </div>
          </div>
        </div>

        <!-- Git commit table show only on big screens-->
        <div class="relative mt-3">
          <div
            class="absolute inset-0 rounded-md border border-[#64ffda]"
          ></div>
          <!-- commits -->
          <div
            class="bg-white rounded-md p-5 md:shadow-md transition ease-in duration-150 hover:-translate-x-3 hover:-translate-y-3 h-full -translate-y-2 -translate-x-2"
          >
            <div class="grid grid-cols-12 gap-1">
              <span
                v-for="i in 36"
                class="p-1 w-full aspect-square rounded"
                :class="GitColor()"
              ></span>
            </div>
            <a
              href="https://github.com/sardorml"
              class="flex justify-end mt-2 items-center text-slate-700 text-sm"
            >
              <span class="underline">Visit github profile</span>
              <nuxt-icon
                name="humbleicons/external-link"
                filled
                class="pl-1 text-lg flex items-center"
              />
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
// function to return random string from an array of 3 strings
const GitColor = computed(() => () => {
  let arr = [
    "bg-gray-200",
    "bg-green-200",
    "bg-green-400",
    "bg-green-600",
    "bg-green-800",
  ];
  return arr[Math.floor(Math.random() * arr.length)];
});
</script>
