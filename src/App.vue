<script setup lang="ts">
import CreationsSection from './components/CreationsSection.vue'
import HelloWorld from './components/CreationsSection.vue'
import LandingSection from './components/LandingSection.vue'
import FooterSection from './components/FooterSection.vue'
</script>

<template>
  <LandingSection />
  <div class="interactive-leader">
    <img class="desktop" src="./assets/desktop/image-interactive.jpg" />
    <img class="mobile" src="./assets/mobile/image-interactive.jpg" />

    <div>
      <h2>The leader in interactive VR</h2>
      <p>
        Founded in 2011, Loopstudios has been producing world-class virtual reality projects for
        some of the best companies around the globe. Our award-winning creations have transformed
        businesses through digital experiences that bind to their brand.
      </p>
    </div>
  </div>
  <CreationsSection />
  <FooterSection />
</template>

<style scoped lang="scss">
.interactive-leader {
  margin: 9rem 9rem 0;
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr;
  align-items: end;

  img.mobile {
    display: none;
  }
  img.desktop {
    grid-row: 1 / 4;
    grid-column: 1 / 5;
  }
  div {
    background-color: white;
    padding: 3rem 0 0 6rem;
    grid-row: 2 / 4;
    grid-column: 2 / 5;
    p {
      opacity: 0.5;
    }
  }
}

@media (max-width: 1350px) {
  .interactive-leader {
    margin: 3rem 3rem 0;

    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
    text-align: center;

    img.desktop {
      display: none;
    }
    img.mobile {
      display: block;
      grid-row: 1;
      grid-column: 1;
      margin: auto;
      max-width: 100%;
    }
    div {
      padding: 0;
      grid-row: 2;
      grid-column: 1;
    }
  }
}
</style>
