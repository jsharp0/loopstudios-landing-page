<script setup lang="ts">
import CreationItem from './CreationItem.vue'
</script>

<script lang="ts">
export default {
  data() {
    return {
      imagePath: `src/assets/${window.innerWidth > 1350 ? 'desktop' : 'mobile'}`,
      showBottomButton: window.innerWidth <= 1350
    }
  },
  computed: {
    showButton() {
      this.showBottomButton = window.innerWidth <= 1350
      return this.showBottomButton
    }
  },

  mounted() {
    this.$nextTick(() => {
      window.addEventListener('resize', this.onResize)
    })
  },

  beforeUnmount() {
    window.removeEventListener('resize', this.onResize)
  },

  methods: {
    onResize() {
      this.imagePath = `src/assets/${window.innerWidth > 1350 ? 'desktop' : 'mobile'}`
    }
  }
}
</script>

<template>
  <div class="creations">
    <div class="heading">
      <h2>OUR CREATIONS</h2>
      <button class="top-btn">SEE ALL</button>
    </div>

    <div class="item-grid">
      <CreationItem label="Deep Earth" imageClass="deep-earth" />
      <CreationItem label="Night Arcade" imageClass="night-arcade" />
      <CreationItem label="Soccer Team VR" imageClass="soccer-team" />
      <CreationItem label="The Grid" imageClass="grid" />
      <CreationItem label="From up above vr" imageClass="from-above" />
      <CreationItem label="Pocket Borealis" imageClass="pocket-borealis" />
      <CreationItem label="The Curiosity" imageClass="curiosity" />
      <CreationItem label="Make it Fisheye" imageClass="fisheye" />
    </div>

    <div class="button-container">
      <button class="bottom-btn">SEE ALL</button>
    </div>
  </div>
</template>

<style scoped lang="scss">
.creations {
  padding: 10rem;
}
button {
  background-color: white;
  border: 1px solid black;
  padding: 0.75rem 2rem;
  letter-spacing: 0.3125rem;
  align-self: center;

  &:hover {
    background-color: black;
    border: 1px solid white;
    color: white;
    cursor: pointer;
  }
}

.heading {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.item-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.5rem;
}
.bottom-btn {
  display: none;
}

@media (max-width: 1350px) {
  .creations {
    padding: 1.5rem;
  }
  .heading {
    justify-content: center;

    .top-btn {
      display: none;
    }
  }

  .button-container {
    width: 100%;
    margin-top: 2rem;
    margin-bottom: 6rem;

    .bottom-btn {
      display: block;
      margin: auto;
    }
  }
  .item-grid {
    grid-template-columns: 1fr;
  }
}
</style>
