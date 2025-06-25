<template>
  <div class="sphere">
    <img :src="sphere" />
  </div>
</template>

<script lang="ts" setup>
import sphere from '../assets/sphere.png';
</script>

<style scoped>
.sphere {
  position: absolute;

  bottom: 0;
  left: -185px;
  width: 391px;
  height: 391px;
}

@media(min-width: 480px) {
  .sphere {
    width: 545px;
    height: 545px;
    bottom: -15px;
    left: -236px;
  }
}

@media(min-width: 640px) {
  .sphere {
    width: 840px;
    height: 840px;
    bottom: -37px;
    left: -389px;
  }
}

@media(min-width: 960px) {
  .sphere {
    width: 978px;
    height: 978px;
    bottom: -46px;
    left: -356px;
  }
}

@media(min-width: 1440px) {
  .sphere {
    width: 777px;
    height: 777px;
    bottom: 0;
    left: -74px;
  }
}

img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}
</style>
