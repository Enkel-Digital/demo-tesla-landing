<template>
  <div id="app">
    <!-- Only 1 hero section for entire landing page -->
    <section class="hero is-fullheight">
      <HeroHead />
      <HeroBody />
      <HeroFooter />
    </section>
  </div>
</template>

<script>
import HeroHead from "@/components/HeroHead";
import HeroBody from "@/components/HeroBody";
import HeroFooter from "@/components/HeroFooter";

export default {
  name: "App",
  components: {
    HeroHead,
    HeroBody,
    HeroFooter,
  },
};
</script>

// Load the bulma styles in the top level component
<style lang="sass" src="bulma" />

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

/* Change background depending on screen size */
.hero {
  background: black url(./assets/images/hero-lg.jpg) center / cover;
}
@media (max-width: 1024px) {
  .hero {
    background: black url(./assets/images/hero-md.jpg) center / cover;
  }
}
@media (max-width: 768px) {
  .hero {
    background: black url(./assets/images/hero-sm.jpg) center / cover;
  }
}

/* Reduce font size on mobile */
@media (max-width: 768px) {
  :root {
    font-size: 90%;
  }
}
</style>
