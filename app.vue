<template>
  <Navigation :class="{ '-translate-y-full': showFullNav }" />
  <div class="container py-60">
    <NuxtPage />
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue";
const scrollPosition = ref(0);
const showFullNav = ref(false);

const handleScroll = () => {
  if (process.client) {
    var currentScrollPosition = window.scrollY;

    if (currentScrollPosition < scrollPosition.value) {
      showFullNav.value = false;
    } else {
      showFullNav.value = true;
    }

    scrollPosition.value = window.scrollY;
  }
};

onMounted(() => {
  if (process.client) {
    window.addEventListener("scroll", handleScroll);
  }
});
onUnmounted(() => {
  if (process.client) {
    window.removeEventListener("scroll", handleScroll);
  }
});
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Bitter:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap");
@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&display=swap");
body {
  /* font-family: Bitter, sans-serif !important; */
  font-family: "Calibre", "Inter", "San Francisco", "SF Pro Text", -apple-system,
    system-ui, sans-serif;
  background-color: #0a192f;
}
.nuxt-icon > svg {
  margin-bottom: 0px !important;
}
</style>
