<template>
  <div class="sphere">
    <img :src="sphere" />
  </div>
</template>

<script lang="ts" setup>
import sphere from '../assets/sphere.png';
</script>

<style lang="scss" scoped>
.sphere {
  position: absolute;
  bottom: 0;
  left: -216px;
  width: 391px;
  height: 391px;

  @media(min-width: 480px) {
    width: 545px;
    height: 545px;
    bottom: -30px;
    left: -281px;
  }

  @media(min-width: 640px) {
    width: 840px;
    height: 840px;
    bottom: -91px;
    left: -459px;
  }

  @media(min-width: 960px) {
    width: 978px;
    height: 978px;
    bottom: -54px;
    left: -461px;
  }

  @media(min-width: 1440px) {
    width: 777px;
    height: 777px;
    bottom: 7px;
    left: -129px;
  }
}

img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}
</style>
