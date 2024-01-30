<template>
  <div class="skills pt-28 pb-48" id="skills">
    <div class="lg:mx-40 md:mx-32">
      <h1
        class="lg:text-3xl text-2xl text-white font-medium mb-28 whitespace-nowrap text-center flex items-center justify-center"
      >
        <span class="bg-slate-500 w-full h-px mr-6"></span>
        <span>What I offer</span>
        <span class="bg-slate-500 w-full h-px ml-6"></span>
      </h1>
    </div>
    <div class="xl:mx-20">
      <div
        v-for="item in services"
        class="mt-20 group hover:cursor-pointer"
        v-motion-slide-visible-bottom
      >
        <h1 class="text-white text-2xl">{{ item.title }}</h1>
        <div
          class="bg-[#112240] rounded-lg p-4 mt-3 flex flex-col lg:flex-row items-center"
        >
          <div
            class="bg-slate-900 rounded-lg flex justify-center items-center lg:w-40 w-full h-40"
          >
            <span class="text-xl text-slate-100 group-hover:text-teal-300">{{
              item.icon
            }}</span>
          </div>

          <div class="flex flex-col justify-center ml-5 mt-5 lg:mt-0">
            <p class="text-slate-400 group-hover:text-slate-300 text-lg">
              {{ item.content }}
            </p>
            <ul class="mt-2 flex flex-wrap">
              <li class="mr-1.5 mt-2" v-for="tool in item.skills">
                <div
                  class="flex items-center rounded-full bg-teal-300/5 hover:bg-teal-400/10 px-4 py-2 text-md font-medium leading-5 text-slate-200 hover:text-teal-300"
                >
                  {{ tool }}
                </div>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
const services = ref([
  {
    title: "Frontend UI interfaces",
    content:
      "I will translate your designs into high quality code, using the latest technologies.",
    icon: "_frontend",
    skills: [
      "React",
      "Next",
      "React Native",
      "Vue",
      "Nuxt",
      "Tailwind",
      "HTML/CSS",
    ],
  },
  {
    title: "Backend Api Services",
    content:
      "I will build the robust and secure foundation your digital projects need to thrive.",
    icon: "_backend",
    skills: ["Node", "Express", "MongoDB", "PostgreSQL", "GraphQL", "REST API"],
  },
  {
    title: "Blockchain Development",
    content:
      "I will help you build your decentralized applications on Ethereum, Polygon, Bincance and other EVM Chains.",
    icon: "_web3",
    skills: [
      "Solidity",
      "Smart Contracts",
      "Web3",
      "Ethereum",
      "Binance Smart Chain",
      "Polygon",
    ],
  },
  {
    title: "Full-Stack Development",
    content:
      "I will create complete web solutions, from frontend design to backend functionality.",
    icon: "_fullstack",
    skills: [
      "Mobile apps",
      "Web apps",
      "Desktop apps",
      "Blockchain apps",
      "APIs",
      "Databases",
    ],
  },
]);
</script>
