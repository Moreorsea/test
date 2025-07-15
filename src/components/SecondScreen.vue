<template>
    <Background>
  <div class="wrapper">
    <Header />
    <div class="grid">

    <h1 class="grid__title">Магический шар предсказывает революцию в работе с ЛНА!</h1>

    <section class="grid__content">
    <!-- <div class="glass grid__text">
      <p>В течение года вы с удивлением обнаружите, что:</p>
      <p>✦  100% сотрудников вовремя знакомятся с локальными актами (и даже не притворяются, что не видели уведомление!)</p>
      <p>✦ Юридические риски сократятся на 90% — больше никаких «Я не знал», «Мне не показывали» и «А где подписать?»</p>
      <p>А когда придет проверка, вы просто выгрузите актуальный лист ознакомления за две минуты — и получите восхищенный взгляд инспектора.</p>
    </div> -->
    <div class="glass grid__text">
      {{ prognose }}
    </div>

    <div class="glass grid__link">
      <h3>Как ускорить исполнение предсказания?</h3>
      <p>Узнайте, как автоматизировать рутину и сделать HR-процессы эффективнее.</p>
      <a class="grid__link-button">Узнать</a>
    </div>
  </section>

    <button class="glass grid__button" @click="$emit('get-repeat-prognose')">Получить новое предсказание</button>
    </div>

    <SecondScreenSphere />
  </div>
</Background>
</template>

<script setup>
import Background from './Background.vue';
import Header from './Header.vue';
import SecondScreenSphere from './SecondScreenSphere.vue';


const props = defineProps({
  prognose: String,
});

defineEmits(['get-repeat-prognose']);
</script>

<style lang="scss" scoped>
// .background {
//   width: 100vw;
//   height: 100vh;
//   background-color: #000611;
//   background-size: cover;
//   background-position: center;
//   background-repeat: no-repeat;
//   background-image: url('../assets/background-320.png');

//   @media(min-width: 480px) {
//     background-image: url('../assets/background-480.png');
//   }

//   @media(min-width: 640px) {
//     background-image: url('../assets/background-640.png');
//   }

//   @media(min-width: 960px) {
//     background-image: url('../assets/background-960.png');
//   }

//   @media(min-width: 1440px) {
//     background-image: url('../assets/background-1440.png');
//   }
// }
.wrapper {
  /* background-image: url('../assets/background-320.png'); */

  //overflow-y: auto;
  // overflow: hidden;
  // padding: 0 14px;
  /* display: grid;
  grid-template-rows: auto 1fr 100px; */
  position: relative;
  width: 256px;
  z-index: 10;

  margin: 0 auto;

  //height: calc(100vh - 45px);

  @media(min-width: 480px) {
    width: 389px;
    //height: calc(100vh - 86px);
  }

  @media(min-width: 640px) {
    width: 500px;
    //height: calc(100vh - 140px);
  }

  @media(min-width: 960px) {
    width: 773px;
    //height: calc(100vh - 155px);
  }

  @media(min-width: 1440px) {
    width: 1330px;
  }
}

.header {
  padding: 20px 0 15px;

  @media(min-width: 480px) {
    padding: 33px 0 15px;
  }

  @media(min-width: 640px) {
    padding: 47px 0 31px;
  }

  @media(min-width: 960px) {
    padding: 61px 0 41px;
  }

  @media(min-width: 1440px) {
    display: flex;
    justify-content: space-between;
  }

  &__logo {
    @media(min-width: 1440px) {
      margin-right: 0;
    }
  }

  &__title {
    img {
      @media(min-width: 1440px) {
        left: 0 !important;
        transform: translateX(0) !important;
      }
    }
  }
}

.grid {
  //position: relative;
 // width: 256px;
  //z-index: 10;
  display: grid;
  //margin: 0 auto;
  //grid-template-rows: 14% 36% calc() 10%;
  //height: 100%;
  grid-template-rows: 19% auto 20%;
  align-content: space-between;
  //height: 100vh;
  height: calc(100vh - 60px);

  @media(min-width: 480px) {
    //width: 389px;
    height: calc(100vh - 110px);
  }

  @media(min-width: 640px) {
    //width: 500px;
    height: calc(100vh - 210px);
  }

  @media(min-width: 960px) {
    //width: 773px;
    height: calc(100vh - 220px);
  }

  @media(min-width: 1440px) {
    height: calc(100vh - 165px);
  }

  &__content {
    @media(min-width: 960px) {
      padding: 0 35px;
    }

    @media(min-width: 1440px) {
      width: 52%;
      margin-left: auto;
      padding: 0;
    }
  }

  &__title {
    font-size: 12px;
    font-weight: 500;
    padding: 0 10px;
    margin-bottom: 26px;

    @media(min-width: 480px) {
      font-size: 18px;
    }

    @media(min-width: 640px) {
      font-size: 24px;
    }

    @media(min-width: 960px) {
      font-size: 40px;
    }

    @media(min-width: 1440px) {
      font-size: 48px;
      text-align: left;
      margin-left: 18px;
    }
  }

  &__text {
    text-align: left;
    font-size: 9px;
    line-height: 10px;
    padding: 8px 12px 0;
    display: flex;
    flex-direction: column;
    align-self: flex-start;
    margin-bottom: 10px;

    @media(min-width: 480px) {
      font-size: 12px;
      line-height: 14px;
      padding: 12px;
      margin-bottom: 20px;
    }

    @media(min-width: 640px) {
      font-size: 16px;
      line-height: 20px;
    }

    @media(min-width: 960px) {
      font-size: 20px;
      line-height: 24px;
      border-radius: 15px;
      padding: 20px 25px;
    }

    & p {
      margin-bottom: 14px;
    }
  }

  h2 {
    display: none;

    @media(min-width: 960px) {
      display: block;
    }
  }

  &__link {
    text-align: left;
    font-weight: 500;
    padding: 7px 8px;
    margin-bottom: 10px;

    @media(min-width: 480px) {
      width: 100%;
      padding: 10px 15px;
    }

    @media(min-width: 960px) {
      border-radius: 15px;
      padding: 20px 20px;
    }

    h3 {
      font-size: 8.5px;
      font-weight: 500;
      letter-spacing: -0.2px;
      font-family: 'VKSansDisplayExpanded', Helvetica, Arial, sans-serif;
      margin-bottom: 5px;
      word-spacing: 1px;

      @media(min-width: 480px) {
        font-size: 13px;
      }

      @media(min-width: 640px) {
        font-size: 17px;
        margin-bottom: 10px;
      }

      @media(min-width: 960px) {
        font-size: 23px;
        margin-bottom: 20px;
      }
    }

    p {
      font-size: 9px;
      margin-bottom: 6px;

      @media(min-width: 480px) {
        font-size: 12px;
      }

      @media(min-width: 640px) {
        font-size: 16px;
        line-height: 20px;
        margin-bottom: 15px;
      }

      @media(min-width: 960px) {
        font-size: 18px;
        margin-bottom: 20px;
      }
    }

    &-button {
      outline: none;
      border: none;
      background-color: #0077FF;
      font-size: 8px;
      border-radius: 5px;
      display: inline-block;
      padding: 5px 13px;
      color: white;
      cursor: pointer;

      @media(min-width: 480px) {
        font-size: 12px;
      }

      @media(min-width: 640px) {
        font-size: 16px;
        padding: 8px 35px;
      }

      @media(min-width: 960px) {
        font-size: 24px;
        padding: 8px 45px;
      }
    }
  }

  &__button {
    font-size: 9.5px;
    display: flex;
    justify-content: flex-end;
    //width: 224px;
    margin-right: -20px;
    margin-left: auto;
    padding: 9px 7px;
    margin-bottom: 20px;
    margin-top: auto;
    //justify-content: flex-end;

    @media(min-width: 480px) {
      font-size: 14px;
      padding: 5px 26px;
    }

    @media(min-width: 640px) {
      font-size: 17px;
      margin-right: -39px;
      padding: 5px 14px;
    }

    @media(min-width: 960px) {
      font-size: 22px;
    }
  }
}
</style>