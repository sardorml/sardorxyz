<template>
  <div class="experience pt-28 pb-48" id="experience">
    <h1
      class="lg:text-3xl text-2xl text-white font-medium mb-28 whitespace-nowrap text-center flex items-center justify-center"
    >
      <span class="bg-slate-500 w-full lg:w-1/4 h-px mr-6"></span>
      <span>What I've worked on</span>
      <span class="bg-slate-500 w-full lg:w-1/4 h-px ml-6"></span>
    </h1>
    <div class="grid grid-cols-1 xl:px-20 gap-y-24">
      <div
        v-for="(experience, index) in experiences"
        class="group lg:-space-x-14 grid grid-cols-1 lg:grid-cols-2 items-center border-indigo-600 rounded-md"
        :class="{ 'lg:space-x-reverse': index % 2 == 0 }"
      >
        <div
          v-motion
          :initial="
            index % 2 == 0 ? { opacity: 0, x: 100 } : { opacity: 0, x: -100 }
          "
          :visible="{ opacity: 1, x: 0 }"
          :class="{ 'lg:order-last': index % 2 == 0 }"
          class="group/image relative max-md:order-last max-md:mt-10"
        >
          <a
            :href="experience.link"
            target="_blank"
            class="lg:hidden flex group-hover/image:flex absolute bg-slate-800 w-full h-full z-10 opacity-90 cursor-pointer justify-center items-center transition ease-in-out duration-300"
          >
            <nuxt-icon
              name="humbleicons/external-link"
              filled
              class="text-white text-5xl"
            />
          </a>
          <img
            :src="`/images/exp/${experience.image}.png`"
            alt="Frontend Development"
            style="object-fit: contain"
          />
        </div>
        <div
          v-motion
          :initial="
            index % 2 == 0 ? { opacity: 0, x: -100 } : { opacity: 0, x: 100 }
          "
          :visible="{ opacity: 1, x: 0 }"
          class="flex flex-col justify-between z-20 mt-6 lg:mt-0"
          :class="index % 2 == 0 ? 'items-start' : 'lg:items-end'"
        >
          <a
            target="_blank"
            :href="experience.companyLink"
            class="flex items-center md:text-2xl text-xl font-medium py-3 text-slate-200 cursor-pointer hover:text-teal-300"
          >
            <span>{{ experience.title }}</span>
            <nuxt-icon name="humbleicons/external-link" filled class="pl-1" />
          </a>
          <p
            class="text-slate-400 bg-[#112240] rounded-md p-5 text-md drop-shadow-2xl"
          >
            {{ experience.description }}
          </p>
          <div>
            <ul class="mt-2 flex flex-wrap">
              <li class="mr-1.5 mt-2" v-for="tool in experience.tools">
                <div
                  class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
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

const experiences = ref([
  {
    image: "lot",
    title: "Wizpace",
    description:
      "Led development of the League of Traders platform using Vuejs and TypeScript.",
    tools: ["Vue", "TypeScript", "NodeJs", "Git CI/CD"],
    link: "https://leagueoftraders.io",
    companyLink: "https://wizpace.com",
  },
  {
    image: "uzumbank",
    title: "Tune Consulting",
    description:
      "Developed uzumbank.uz, a banking app, with a focus on efficiency using Vue.js and Vuex.",
    tools: ["Vue", "TypeScript", "NodeJs", "Git CI/CD"],
    link: "https://uzumbank.uz",
    companyLink: "https://tuneconsulting.net/",
  },
  {
    image: "metamui",
    title: "MetaMUI",
    description:
      "Maintained and improved features of a mobile crypto wallet app using React Native, implemented a wallet recovery tool with Node.js, and enhanced security for Firebase database.",
    tools: ["React Native", "TypeScript", "NodeJs", "Firebase"],
    link: "https://sovereignwallet.network",
    companyLink: "https://sovereignwallet.network",
  },
  {
    image: "xailand",
    title: "Xailand",
    description:
      "Contributed to building a dashboard for an AI appraisal platform, catering to realtors and land buyers.",
    tools: ["Vue", "TypeScript", "NodeJs", "Git CI/CD", "AWS"],
    link: "https://xai.land",
    companyLink: "https://xai.land",
  },
  {
    image: "sucartv",
    title: "CID Auto",
    description:
      "Developed a listings website for used cars using Vue.js, created an API with Node.js/Express, and designed an AWS cloud function for video files.",
    tools: ["Vue", "TypeScript", "NodeJs", "AWS"],
    link: "https://tracxn.com/d/companies/cid-auto/__Qpr_vfJGZOtCh56Mv6lRVNYFXbwckLOIMxdTglPmodA",
    companyLink: "https://www.crunchbase.com/organization/cid-auto",
  },
]);
</script>
