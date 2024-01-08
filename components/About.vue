<template>
  <div class="skills pt-28 pb-48" id="about">
    <div class="lg:mx-40 md:mx-32 mb-48">
      <h1
        class="lg:text-3xl text-2xl text-white font-medium whitespace-nowrap text-center flex items-center justify-center"
      >
        <span class="bg-slate-500 w-full h-px mr-6"></span>
        <span>About Me</span>
        <span class="bg-slate-500 w-full h-px ml-6"></span>
      </h1>
    </div>

    <div class="lg:mx-28 lg:flex-row flex flex-col items-center">
      <!-- about me card -->
      <!-- <div class="bg-white h-80 w-80 rounded-md flex-none"></div> -->
      <img
        v-motion-slide-visible-left
        src="/images/hero/portrait.jpeg"
        alt="Sardor Mamadaliev"
        class="w-80 rounded-md shadow-2xl flex-none v-motion-roll-visible-bottom mb-10 lg:mb-0"
      />
      <p
        v-motion-slide-visible-right
        class="text-lg font-light text-slate-200 ml-10 v-motion-roll-visible-bottom"
      >
        I'm Sardor, a seasoned software developer with hands-on experience in
        the tech industry. At Wizpace, I spearheaded the development of the
        League of Traders platform, successfully launching it within a tight
        timeframe, now serving over 10,000 traders globally. Earlier at Tune
        Consulting, I contributed to the creation of Apelsin.uz, a banking app,
        optimizing efficiency with a Vuejs UI library. My journey also includes
        roles at Nod Bizware, enhancing a mobile crypto wallet app, and CID
        Auto, where I developed a listings website for used cars. Let's connect
        and explore how I can contribute to your next project.
      </p>
    </div>
  </div>
</template>
