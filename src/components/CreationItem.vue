<script>
export default {
  name: 'CreationItem',
  props: {
    imageClass: {
      type: String,
      default: ''
    },

    label: {
      type: String,
      default: ''
    }
  }
}
</script>
<template>
  <div :class="'item ' + imageClass" class="item">
    <h3>{{ label }}</h3>
  </div>
</template>

<style scoped lang="scss">
$gradient: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.6));
$hover-gradient: linear-gradient(rgba(255, 255, 255, 0.75), rgba(255, 255, 255, 0.75));
$desktopPath: '../assets/desktop/';
$mobilePath: '../assets/mobile/';

.item {
  height: 450px;
  display: flex;
  align-items: flex-end;
  padding-left: 2rem;
  color: white;
  cursor: pointer;

  &:hover {
    color: black;
  }

  h3 {
    width: 60%;
  }
}
.deep-earth {
  background: $gradient, url($desktopPath + 'image-deep-earth.jpg');
  background-position: center;
  background-size: cover;
  &:hover {
    background: $hover-gradient, url($desktopPath + 'image-deep-earth.jpg');
    background-position: center;
    background-size: cover;
  }
}

.curiosity {
  background: $gradient, url($desktopPath + 'image-curiosity.jpg');
  background-position: center;
  background-size: cover;

  &:hover {
    background: $hover-gradient, url($desktopPath + 'image-curiosity.jpg');
    background-position: center;
    background-size: cover;
  }
}

.fisheye {
  background: $gradient, url($desktopPath + 'image-fisheye.jpg');
  background-position: center;
  background-size: cover;

  &:hover {
    background: $hover-gradient, url($desktopPath + 'image-fisheye.jpg');
    background-position: center;
    background-size: cover;
  }
}

.from-above {
  background: $gradient, url($desktopPath + 'image-from-above.jpg');
  background-position: center;
  background-size: cover;

  &:hover {
    background: $hover-gradient, url($desktopPath + 'image-from-above.jpg');
    background-position: center;
    background-size: cover;
  }
}

.grid {
  background: $gradient, url($desktopPath + 'image-grid.jpg');
  background-position: center;
  background-size: cover;

  &:hover {
    background: $hover-gradient, url($desktopPath + 'image-grid.jpg');
    background-position: center;
    background-size: cover;
  }
}

.night-arcade {
  background: $gradient, url($desktopPath + 'image-night-arcade.jpg');
  background-position: center;
  background-size: cover;

  &:hover {
    background: $hover-gradient, url($desktopPath + 'image-night-arcade.jpg');
    background-position: center;
    background-size: cover;
  }
}

.pocket-borealis {
  background: $gradient, url($desktopPath + 'image-pocket-borealis.jpg');
  background-position: center;
  background-size: cover;

  &:hover {
    background: $hover-gradient, url($desktopPath + 'image-pocket-borealis.jpg');
    background-position: center;
    background-size: cover;
  }
}

.soccer-team {
  background: $gradient, url($desktopPath + 'image-soccer-team.jpg');
  background-position: center;
  background-size: cover;

  &:hover {
    background: $hover-gradient, url($desktopPath + 'image-soccer-team.jpg');
    background-position: center;
    background-size: cover;
  }
}

@media (max-width: 1350px) {
  .deep-earth {
    background: $gradient, url($mobilePath + 'image-deep-earth.jpg');
    background-position: center;
    background-size: cover;
    &:hover {
      background: $hover-gradient, url($mobilePath + 'image-deep-earth.jpg');
      background-position: center;
      background-size: cover;
    }
  }

  .curiosity {
    background: $gradient, url($mobilePath + 'image-curiosity.jpg');
    background-position: center;
    background-size: cover;

    &:hover {
      background: $hover-gradient, url($mobilePath + 'image-curiosity.jpg');
      background-position: center;
      background-size: cover;
    }
  }

  .fisheye {
    background: $gradient, url($mobilePath + 'image-fisheye.jpg');
    background-position: center;
    background-size: cover;

    &:hover {
      background: $hover-gradient, url($mobilePath + 'image-fisheye.jpg');
      background-position: center;
      background-size: cover;
    }
  }

  .from-above {
    background: $gradient, url($mobilePath + 'image-from-above.jpg');
    background-position: center;
    background-size: cover;

    &:hover {
      background: $hover-gradient, url($mobilePath + 'image-from-above.jpg');
      background-position: center;
      background-size: cover;
    }
  }

  .grid {
    background: $gradient, url($mobilePath + 'image-grid.jpg');
    background-position: center;
    background-size: cover;

    &:hover {
      background: $hover-gradient, url($mobilePath + 'image-grid.jpg');
      background-position: center;
      background-size: cover;
    }
  }

  .night-arcade {
    background: $gradient, url($mobilePath + 'image-night-arcade.jpg');
    background-position: center;
    background-size: cover;

    &:hover {
      background: $hover-gradient, url($mobilePath + 'image-night-arcade.jpg');
      background-position: center;
      background-size: cover;
    }
  }

  .pocket-borealis {
    background: $gradient, url($mobilePath + 'image-pocket-borealis.jpg');
    background-position: center;
    background-size: cover;

    &:hover {
      background: $hover-gradient, url($mobilePath + 'image-pocket-borealis.jpg');
      background-position: center;
      background-size: cover;
    }
  }

  .soccer-team {
    background: $gradient, url($mobilePath + 'image-soccer-team.jpg');
    background-position: center;
    background-size: cover;

    &:hover {
      background: $hover-gradient, url($mobilePath + 'image-soccer-team.jpg');
      background-position: center;
      background-size: cover;
    }
  }
}
</style>
