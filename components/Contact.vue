<template>
  <div class="contact pt-28 pb-96" id="contact">
    <h1
      class="md:text-3xl text-2xl text-slate-200 font-medium flex justify-center items-center mb-28 whitespace-nowrap"
    >
      <span>Get in touch</span>
    </h1>
    <div class="flex justify-center items-center">
      <a href="mailto:sardormdl@gmail.com" v-motion-roll-visible-left>
        <nuxt-icon
          name="feathericons/mail"
          filled
          class="text-slate-300 text-7xl hover:text-teal-300"
        />
      </a>

      <a
        href="https://www.linkedin.com/in/sardorml/"
        target="_blank"
        class="ml-4"
        v-motion-roll-visible-right
      >
        <nuxt-icon
          name="feathericons/linkedin"
          filled
          class="text-slate-300 text-7xl hover:text-teal-300"
        />
      </a>
    </div>
  </div>
</template>
