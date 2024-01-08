<script lang="ts">
export default {
  methods: {
    toggleMenu() {
      const menu = document.querySelector('.menu')
      if (menu) {
        menu.classList.toggle('open')
      }
    }
  }
}
</script>
<template>
  <div class="landing">
    <nav class="light">
      <img src="../assets/logo.svg" />
      <img class="menu-toggle" src="../assets/icon-hamburger.svg" @click="toggleMenu" />
      <ul>
        <li>About</li>
        <li>Careers</li>
        <li>Events</li>
        <li>Products</li>
        <li>Support</li>
      </ul>
    </nav>
    <div class="menu">
      <div>
        <img src="../assets/logo.svg" />
        <img class="menu-close" src="../assets/icon-close.svg" @click="toggleMenu" />
      </div>
      <ul>
        <li><h3>About</h3></li>
        <li><h3>Careers</h3></li>
        <li><h3>Events</h3></li>
        <li><h3>Products</h3></li>
        <li><h3>Support</h3></li>
      </ul>
    </div>
    <h1 class="site-heading light">Immersive experiences that deliver</h1>
  </div>
</template>

<style scoped lang="scss">
.landing {
  background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
    url('../assets/desktop/image-hero.jpg');
  height: 650px;
  padding: 4rem 10rem;
  background-repeat: no-repeat;
  background-size: cover;
}

.site-heading {
  border: 2px solid white;
  padding: 2.5rem;
  max-width: 650px;
}

.menu-toggle,
.menu {
  display: none;
}

nav {
  display: flex;
  justify-content: space-between;
  margin-bottom: 8rem;
  img {
    align-self: center;
  }
  ul {
    list-style: none;
    display: flex;
    li:not(:last-child) {
      margin-right: 2rem;
    }
    li:hover {
      text-decoration: underline;
      cursor: pointer;
    }
  }
}
@media (max-width: 1350px) {
  .landing {
    padding: 4rem 1.5rem;
  }
  .menu-toggle {
    display: block;
    cursor: pointer;
  }

  .site-heading {
    max-width: 100%;
  }
  nav ul {
    display: none;
  }
  .menu.open {
    padding: 2.5rem 1.5rem;
    background-color: black;
    color: white;
    display: block;
    width: 95%;
    position: absolute;
    height: 650px;
    top: 0;
    left: 0;

    ul {
      margin-top: 10rem;
      text-align: center;
      list-style: none;
      li:not(:last-child) {
        margin-bottom: 2rem;
      }
      li:hover {
        text-decoration: underline;
        cursor: pointer;
      }
    }

    div {
      display: flex;
      align-items: center;
      justify-content: space-between;

      img {
        align-self: center;
        cursor: pointer;
      }
    }
  }
}
</style>
