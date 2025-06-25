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
  left: 50%;
  bottom: 90px;
  transform: translateX(-50%);
  width: 278px;
  height: 278px;
}

@media(min-width: 480px) {
  .sphere {
    width: 377px;
    height: 377px;
    bottom: 122px;
  }
}

@media(min-width: 640px) {
  .sphere {
    width: 509px;
    height: 509px;
    bottom: 248px;
  }
}

@media(min-width: 960px) {
  .sphere {
    width: 703px;
    height: 703px;
    bottom: 185px;
  }
}

@media(min-width: 1440px) {
  .sphere {
    width: 783px;
    height: 783px;
    bottom: -3px;
  }
}

img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}
</style>
