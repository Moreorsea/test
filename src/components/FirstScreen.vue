<template>
  <Background>
  <div class="wrapper">
    <!-- <img
      class="background"
      src="../assets/background-320.png"
      srcset="
           ../assets/background-320.png 320w,
           ../assets/background-480.png 480w,
           ../assets/background-640.png 640w,
           ../assets/background-960.png 960w,
           ../assets/background-1440.png 1440w"
      sizes="(min-width: 1440px) 1440px,
           (min-width: 960px) 960px,
           (min-width: 640px) 640px,
           (min-width: 480px) 480px,
           320px"
      alt="Адаптивный фон"
      loading="lazy"
    > -->
    <!-- background: linear-gradient(180.15deg, rgba(0, 0, 0, 0) 37.56%, #000000 69.23%);
 -->
  <Header />

  <h1 class="grid-title">Загляните <br />в ваше HR-будущее</h1>

  <div class="grid">


  <div class="row-first">
        <button class="glass glass-label glass-label--left">Какие возможности откроются для вас в ближайшее время... </button>
      </div>

      <div class="row-second">
        <button class="glass glass-label glass-label--right">И что нужно сделать, чтобы удачное предсказание стало реальностью...</button>
      </div>


      <Sphere />
      </div>
      <div class="grid-footer">
        <button class="glass glass-btn" @click="$emit('get-prognose')">Получить предсказание</button>
      </div>
  </div>
</Background>
</template>

<script setup>
import Header from './Header.vue';
import Sphere from './Sphere.vue';
import Background from './Background.vue';

defineEmits(['get-prognose']);
</script>

<style lang="scss" scoped>
.wrapper {
  width: 100vw;
  height: 100vh;
  //background-color: #000611;
  /* background-image: url('../assets/background-320.png'); */
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  overflow: hidden;
  display: grid;
  grid-template-rows: auto auto 1fr 86px;

  @media(min-width: 480px) {
    grid-template-rows: auto auto 1fr 112px;
  }

  @media(min-width: 640px) {
    grid-template-rows: auto auto 1fr 188px;
  }

  @media(min-width: 1440px) {
    grid-template-rows: auto auto 1fr 214px;
  }
}

.grid {
  width: 286px;
  margin: auto;
  //display: grid;
  //grid-template-rows: 31% 34% calc(100% - 31% - 34%);
  display: flex;
  flex-direction: column;

  @media(min-width: 480px) {
    grid-template-rows: 36% 23% calc(100% - 36% - 23%);
    width: 419px;
  }

  @media(min-width: 640px) {
    width: 570px;
  }

  @media(min-width: 960px) {
    width: 875px;
  }

  @media(min-width: 1440px) {
    width: 1346px;
  }

  &-title {
    //margin-bottom: 69px;

    @media(min-width: 480px) {
      //margin-bottom: 115px;
      //margin-bottom: 7.1rem;
      //margin-bottom: 27%;
    }

    @media(min-width: 640px) {
      //margin-bottom: 154px;
    }

    @media(min-width: 960px) {
      //margin-bottom: 126px;
    }

    @media(min-width: 1440px) {
      //margin-bottom: 177px;
    }
  }

  &-footer {
    font-size: 12.5px;
    padding-top: 10px;

    @media(min-width: 480px) {
      margin-top: 0;
    }

    @media(min-width: 1440px) {
      display: flex;
      justify-content: flex-end;
      align-items: flex-start;
    }

    .glass {
      padding: 7px 10px 9px;
      background: rgba(255, 255, 255, 0.1);
      font-weight: 400;

      @media(min-width: 480px) {
        font-size: 15px;
        padding: 9px 15px;
      }

      @media(min-width: 640px) {
        font-size: 28px;
        padding: 18px 20px 22px;
      }

      @media(min-width: 960px) {
        font-size: 38px;
        padding: 30px 20px;
      }

      @media(min-width: 1440px) {
        font-size: 29px;
        margin-right: 3%;
        padding: 22px 34px;
      }
    }
  }


}


// .background {
//   position: absolute;
//   top: 0;
//   left: 0;
//   width: 100%;
//   height: 100%;
//   object-fit: cover;
// }

@media(min-width: 1440px) {
  /* .wrapper {
    background-image: url('../assets/background-1440.png');
  } */
}

.row-first {
  display: flex;
  justify-content: flex-start;
  margin-left: 4%;
  margin-bottom: 69px;
  //margin-bottom: 4.2rem;

  @media(min-width: 480px) {
    margin-left: 0;
    //margin-bottom: 56px;
    //margin-bottom: 3.7rem;
    //margin-bottom: 14%;
  }

  @media(min-width: 640px) {
    margin-bottom: 87px;
  }

  @media(min-width: 960px) {
    margin-bottom: 150px;
  }

  @media(min-width: 1440px) {
    margin-bottom: 64px;
  }

  .glass {
    border-radius: 3px;
    padding: 8px 10px 12px;
    letter-spacing: 0.5px;
    width: 170px;
    font-weight: 400;
    display: flex;
    align-self: baseline;

    @media(min-width: 480px) {
      font-size: 13px;
      width: 231px;
      border-radius: 7px;
      padding: 11px 10px 12px;
    }

    @media(min-width: 640px) {
      font-size: 18px;
      margin-left: 3%;
      width: 310px;
    }

    @media(min-width: 960px) {
      font-size: 26px;
      margin-left: 1.5%;
      width: 460px;
      padding: 21px 10px 12px;
    }

    @media(min-width: 1440px) {
      margin-left: 3%;
      padding: 21px 10px 24px;
    }
  }
}

.row-second {
  display: flex;
  justify-content: flex-end;
  //margin-bottom: 20px;

  @media(min-width: 640px) {}

  .glass {
    border-radius: 3px;
    padding: 8px 7px 12px;
    letter-spacing: 0.5px;
    width: 190px;
    display: flex;
    align-self: baseline;

    @media(min-width: 480px) {
      font-size: 13px;
      width: 253px;
      letter-spacing: 0;
      padding: 10px 7px 12px;
    }

    @media(min-width: 640px) {
      font-size: 18px;
      width: 345px;
    }

    @media(min-width: 960px) {
      font-size: 24px;
      width: 456px;
      padding: 16px 7px 22px;
    }

    @media(min-width: 1440px) {
      width: 516px;
      font-size: 25px;
      padding: 23px 7px 29px;
    }
  }
}



</style>