<template>
  <div class="container">
    <!-- <Header /> -->

    <SecondScreen
      v-if="prognose"
      :prognose="prognose.text"
      @get-repeat-prognose="getSecondPrognose" />

    <FirstScreen v-else @get-prognose="getPrognose" />
    <!-- <Sphere /> -->
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
import FirstScreen from './FirstScreen.vue';
import SecondScreen from './SecondScreen.vue';
import Header from './Header.vue';
import Sphere from './Sphere.vue';

import { hr_predictions, hr_repeat_predications} from '../mock/prognoses.json';

const prognose = ref('');
console.log('PROG', hr_predictions)

const getPrognose = () => {
  prognose.value = hr_predictions[Math.floor(Math.random() * hr_predictions.length)];
}

const getSecondPrognose = () => {
  prognose.value = hr_repeat_predications[Math.floor(Math.random() * hr_repeat_predications.length)];
}
</script>

<style>

.button {
  font-size: 12.5px;
  position: relative;
  z-index: 10;
  border: 0.31px solid;
  border-image-source: linear-gradient(265.43deg, #FFFFFF 0.74%, rgba(255, 255, 255, 0) 53.7%);
  backdrop-filter: blur(6.727431774139404px);
  padding: 20px;
  border-radius: 6px;
}

.glass {
  /* Текст */
  color: white;
  font-weight: 500;
  position: relative;
  z-index: 10;

  /* Размытый фон */
  background: rgba(0, 0, 0, 0.3);
  backdrop-filter: blur(6px);
  -webkit-backdrop-filter: blur(6px);

  /* Границы и форма */
  border: none;

  border-radius: 6px;
  padding: 12px 24px;

  /* Эффекты */
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  display: inline-block;

  /* Дополнительно */
  cursor: pointer;
  outline: none;
  overflow: hidden;
  font-family: 'VKSansDisplay';
}

/* @media(min-width: 480px) {
  .glass {
    font-size: 7px;
  }
}

@media(min-width: 640px) {
  .glass {
    font-size: 10px;
  }
}

@media(min-width: 960px) {
  .glass {
    font-size: 15px;
  }
}

@media(min-width: 1440px) {
  .glass {

  }
} */



/* .glass-label--right {
  width: 190px;
}

@media(min-width: 480px) {
  .glass-label--right {
    font-size: 7px;
  }
}

@media(min-width: 640px) {
  .glass-label--right {
    font-size: 10px;
  }
}

@media(min-width: 960px) {
  .glass-label--right {
    font-size: 15px;
  }
} */

@media(min-width: 1440px) {
  .glass-label--right {

  }
}

.glass-btn {}

.glass-label {
  font-size: 9px;
}

@media(min-width: 480px) {
  .glass-label {
    font-size: 14px;
  }
}

@media(min-width: 640px) {
  .glass-label {
    font-size: 18px;
  }
}

@media(min-width: 960px) {
  .glass-label {
    font-size: 23px;
  }
}

@media(min-width: 1440px) {
  .glass-label {
    font-size: 27px;
  }
}

.glass:hover {
  background: rgba(255, 255, 255, 0.3);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
}

.glass:active {
  transform: translateY(1px);
}

/* Псевдоэлемент для рамки */
/* .glass::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border-radius: 12px;

    box-shadow:
      inset 1px 0 0 0 rgba(255, 255, 255, 0.8),
      inset 0 1px 0 0 rgba(255, 255, 255, 0.8);


    filter: blur(0.5px);
    transition: all 0.6s cubic-bezier(0.16, 1, 0.3, 1);
    pointer-events: none;
  } */

  /* Эффект при наведении */
.glass:hover::before {
     box-shadow:
      inset 2px 0 0 0 rgba(255, 255, 255, 0.8),
      inset 0 2px 0 0 rgba(255, 255, 255, 0.8),
      inset -2px 0 0 0 rgba(255, 255, 255, 0.4),
      inset 0 -2px 0 0 rgba(255, 255, 255, 0.4);

    /* Усиление размытия */
    filter: blur(1.5px);
  }

.glass-btnbox-shadow:active::before {
    box-shadow:
      inset 3px 0 0 0 rgba(255, 255, 255, 0.9),
      inset 0 3px 0 0 rgba(255, 255, 255, 0.9),
      inset -3px 0 0 0 rgba(255, 255, 255, 0.5),
      inset 0 -3px 0 0 rgba(255, 255, 255, 0.5);
  }

.second-button {
  padding: 12px 24px;
  border: none;
  border-radius: 8px;
  background: white;
  position: relative;
  color: #333;
  font-weight: bold;
  cursor: pointer;
  outline: none;
  font-size: 50px;
}


.second-button::before {
    content: '';
    position: absolute;
    top: -2px;
    left: -2px;
    right: -2px;
    bottom: -2px;
    background: linear-gradient(45deg, #ff8a00, #da1b60, #ff8a00);
    background-size: 200% 200%;
    border-radius: 10px;
    z-index: -1;
    transition: all 0.3s ease;
  }

h1 {
  font-size: 16px;
  line-height: 110%;
  font-family: 'VKSansDisplayExpanded', Helvetica, Arial, sans-serif;
  font-weight: 700;
  z-index: 10;
  position: relative;
}

@media(min-width: 480px) {
  h1 {
    font-size: 23px;
  }
}

@media(min-width: 640px) {
  h1 {
    font-size: 33px;
  }
}

@media(min-width: 960px) {
  h1 {
    font-size: 56px;
  }
}
/*
.wrapper {
  overflow: hidden;
} */
</style>