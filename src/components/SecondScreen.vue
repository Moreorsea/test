<template>
  <div class="wrapper">
    <Header />

    <!-- <h2>Магический шар предсказывает революцию в работе с ЛНА!</h2>

    <div class="glass">
      В течение года вы с удивлением обнаружите, что:

    ✦  100% сотрудников вовремя знакомятся с локальными актами (и даже не притворяются, что не видели уведомление!)

    ✦ Юридические риски сократятся на 90% — больше никаких «Я не знал», «Мне не показывали» и «А где подписать?»

    А когда придет проверка, вы просто выгрузите актуальный лист ознакомления за две минуты — и получите восхищенный взгляд инспектора.
    </div>

    <div class="glass">
      Переходите на сайт VK HR Tek и узнайте, как сделать подписание ЛНА прозрачным и удобным.
    </div> -->
    <ScondScreenSphere />

    <button class="glass">Получить новое предсказание</button>
  </div>
</template>

<script setup>
import Header from './Header.vue';
import ScondScreenSphere from './SecondScreenSphere.vue';
</script>

<style scoped>
.wrapper {
  width: 100vw;
  height: 100vh;
  background-color: #000611;
  /* background-image: url('../assets/background-320.png'); */
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  overflow: hidden;
  /* display: grid;
  grid-template-rows: auto 1fr 100px; */
}
</style>