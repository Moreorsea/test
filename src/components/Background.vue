<template>
  <div class="background">
    <slot></slot>
  </div>
</template>

<style lang="scss">
.background {
  width: 100vw;
  height: 100vh;
  background-color: #000611;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-image:
    linear-gradient(180.15deg, rgba(0, 0, 0, 0) 37.56%, #000000 69.23%),
    url('../assets/background-320.png');

  @media(min-width: 480px) {
    background-image: linear-gradient(180.15deg, rgba(0, 0, 0, 0) 37.56%, #000000 69.23%), url('../assets/background-480.png');
  }

  @media(min-width: 640px) {
    background-image: linear-gradient(180.15deg, rgba(0, 0, 0, 0) 37.56%, #000000 69.23%), url('../assets/background-640.png');
  }

  @media(min-width: 960px) {
    background-image: linear-gradient(180.15deg, rgba(0, 0, 0, 0) 37.56%, #000000 69.23%), url('../assets/background-960.png');
  }

  @media(min-width: 1440px) {
    background-image: linear-gradient(180.15deg, rgba(0, 0, 0, 0) 37.56%, #000000 69.23%), url('../assets/background-1440.png');
  }
}
</style>