<template>
  <div id="animation-container" class="animation-container d-flex">
    <div class="horizontal-container">
      <h1 class="vertical-container">+</h1>
    </div>
    <div class="horizontal-container">
      <img src="" alt="" />
    </div>
    <img class="moving-wave" src="/graphics/wave1.svg" alt="wave" />
    <!-- <img class="moving-wave" src="/graphics/wave2.svg" alt="wave" />
    <img class="moving-wave" src="/graphics/wave3.svg" alt="wave" /> -->
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default class Background extends Vue {
  mounted() {}
}
</script>

<style lang="scss" scoped>
.horizontal-container {
  position: absolute;
  top: 50%;
  left: -100px;
  right: calc(100vw + 100px);
  animation: vertical 10s ease-in-out;
  animation-iteration-count: infinite;
}

.vertical-container {
  position: absolute;
  left: 0;
  animation: horizontal 10s linear;
  animation-iteration-count: infinite;
}

.moving-wave {
  width: 100vw;
  object-fit: contain;
  animation: wave 20s ease-in-out;
  animation-iteration-count: infinite;
}

@keyframes horizontal {
  from {
    transform: translateX(-30px);
  }
  to {
    transform: translateX(calc(100vw + 100px));
  }
}

@keyframes vertical {
  0% {
    transform: translateY(-30px);
  }
  50% {
    transform: translateY(80px);
  }
  100% {
    transform: translateY(-30px);
  }
}

@keyframes wave {
  0% {
    transform: scaleY(1);
  }
  50% {
    transform: scaleY(-1);
  }
  100% {
    transform: scaleY(1);
  }
}
</style>
