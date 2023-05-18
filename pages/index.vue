<template>
  <header class="hero-card banner">
    <img src="https://images.pexels.com/photos/2603464/pexels-photo-2603464.jpeg" title="Photo by Aleksandar Pasaric from Pexels: https://www.pexels.com/photo/photo-of-buildings-during-nighttime-2603464/" />
    <div class="gutter text-xl" style="z-index: 99;">
        {{ introText }} <NuxtLink to="/projects">Check out some of my projects</NuxtLink>
    </div>
  </header>

</template>

<script>

  export default {
    data() {
      return {
        introText: "Yo! My name is Anthony Valenzo and I’m a student and aspiring Front End Engineer."
      }
    },

    methods: {
      
    }
  }
</script>