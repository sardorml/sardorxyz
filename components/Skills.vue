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

    <!-- <div class="flex border-b-2 border-white w-full mt-10"></div> -->
    <div
      class="grid grid-cols-1 lg:grid-cols-3 place-content-center gap-3 lg:px-20"
    >
      <div
        class="flex lg:block group cursor-pointer rounded-md m-2 p-4 text-white shadow-[inset_1px_1px_1px_1px_rgba(148,163,184,0.1)] hover:drop-shadow-lg hover:bg-slate-800/50 transition motion-reduce:transition-none"
        v-for="service in services"
      >
        <div class="flex justify-center items-center mx-6 lg:mx-0">
          <nuxt-icon
            :name="service.icon"
            filled
            class="mr-2 text-5xl group-hover:text-teal-300"
          />
        </div>
        <div>
          <h3
            class="md:text-xl text-lg font-medium py-3 text-slate-200 lg:text-center group-hover:text-teal-300"
          >
            {{ service.title }}
          </h3>
          <p class="text-slate-400">{{ service.content }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { ref } from "vue";
const route = useRoute();

const services = ref([
  {
    title: "UI/UX Design",
    content:
      "Crafting user-friendly and visually appealing interfaces to captivate your audience.",
    icon: "humbleicons/switch-on",
  },
  {
    title: "Backend as a Service",
    content:
      "Building the robust and secure foundation your digital projects need to thrive.",
    icon: "humbleicons/database",
  },
  {
    title: "Full-Stack Development",
    content:
      "Creating complete web solutions, from frontend design to backend functionality.",
    icon: "humbleicons/dashboard",
  },
  {
    title: "Website Maintenance",
    content:
      "Improving and sustaining your digital assets for continued success.",
    icon: "humbleicons/cog",
  },
  {
    title: "SEO Optimization",
    content:
      "Boosting your online visibility with SEO strategies and consulting tailored to your goals.",
    icon: "humbleicons/globe",
  },
  {
    title: "Consulting",
    content:
      "Guiding your business strategically with my technical expertise to optimize your digital initiatives.",
    icon: "humbleicons/users",
  },
]);
</script>
