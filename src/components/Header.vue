<template>
  <header class="header">
    <div class="header__logo"></div>

    <div class="header__title">
      <img class="logo" :src="VkLogo" />
    </div>

    <div class="header__tech">
      <img class="header__tech" :src="VkTech" />
    </div>
  </header>
</template>

<script lang="ts" setup>
import VkLogo from '../assets/vk-logo.png';
import VkTech from '../assets/vk-tech.png';
</script>

<style lang="scss" scoped>
.header {
  display: grid;
  grid-template-columns: 33% 33% 33%;
  padding: 20px 15px 15px;
  align-items: center;

  @media(min-width: 480px) {
    padding: 33px 15px 15px;
  }

  @media(min-width: 640px) {
    padding: 45px 15px 21px;
  }

  @media(min-width: 960px) {
    padding: 62px 15px 32px;
  }

  @media(min-width: 1440px) {
    padding: 62px 15px 32px;
  }
}

.header__logo {
  margin-right: auto;
}

.header__tech {
  width: 100%;
  height: 12px;
  position: relative;

  @media(min-width: 480px) {
    height: 18px;
  }

  @media(min-width: 640px) {
    height: 28px;
    margin-right: 15px;
  }

  @media(min-width: 960px) {
    height: 46px;
    margin-right: 21px;
  }

  @media(min-width: 1440px) {
    height: 63px;
    margin-top: -5px;
  }
}

.header__title {
  width: 100%;
  height: 16px;
  position: relative;
}

@media(min-width: 480px) {
  .header__title {
    height: 22px;
  }
}

@media(min-width: 640px) {
  .header__title {
    height: 31px;
  }
}

@media(min-width: 960px) {
  .header__title {
    height: 53px;
  }
}

img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.header__tech img {
  position: absolute;
  right: 0;
  width: auto;
  height: 100%;
  z-index: 10;
}

.header__title img {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  width: auto;
  height: 100%;
  z-index: 10;
}
</style>