<script setup lang="ts"></script>

<template>
  <footer>
    <img src="../assets/logo.svg" />
    <ul class="light">
      <li>About</li>
      <li>Careers</li>
      <li>Events</li>
      <li>Products</li>
      <li>Support</li>
    </ul>
    <div class="icons">
      <img class="icon" src="../assets/icon-facebook.svg" />
      <img class="icon" src="../assets/icon-twitter.svg" />
      <img class="icon" src="../assets/icon-pinterest.svg" />
      <img class="icon" src="../assets/icon-instagram.svg" />
    </div>
    <span class="light">© 2021 Loopstudios. All rights reserved.</span>
  </footer>
</template>

<style scoped lang="scss">
footer {
  background-color: black;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  padding: 2rem 10rem;
  align-items: center;
}

ul {
  padding-left: 0;
  list-style: none;
  display: flex;
  grid-row: 2;

  li:not(:last-child) {
    margin-right: 2rem;
  }

  li:hover {
    text-decoration: underline;
    cursor: pointer;
  }
}
img {
  height: 1.5rem;
}

span {
  opacity: 0.5;
  text-align: right;
}

.icons {
  text-align: right;
}
.icon {
  padding-bottom: 0.5rem;
  border-bottom: 1px solid transparent;
  cursor: pointer;
  &:hover {
    border-bottom: 1px solid white;
  }
  &:not(:last-child) {
    margin-right: 1rem;
  }
}

@media (max-width: 1350px) {
  footer {
    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
    text-align: center;
    justify-items: center;
  }

  ul {
    display: block;
    margin-top: 2rem;
    margin-bottom: 2rem;

    li:not(:last-child) {
      margin-right: 0;
      margin-bottom: 1rem;
    }
  }

  .icons {
    margin-top: 1rem;
    margin-bottom: 1rem;
  }
}
</style>
