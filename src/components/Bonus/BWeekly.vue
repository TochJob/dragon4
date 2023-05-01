<template>
  <div class="weekly wrapper">
    <div class="weekly__main">
      <h3 class="weekly__title">Еженедельный кэшбэк</h3>
      <p class="weekly__text">У вас зачислен кэшбек, нажмите чтоб забрать.</p>
      <div class="wrapper weekly__mult">
        <div class="weekly__factor wrapper">
          <p class="weekly__text weekly__factor-text">Ваш множитель отыгрыша</p>
          <p class="weekly__bonus">x3</p>
        </div>
        <div class="wrapper weekly__total">
          <p class="weekly__bonus weekly__total-text">300 000</p>
          <img src="@/assets/img/coin.png" alt="coin" />
        </div>
      </div>
    </div>
    <AutorisationButton class="weekly__button" />
  </div>
</template>
<script>
import AutorisationButton from '../UI/AutorisationButton.vue';

export default { components: { AutorisationButton } };
</script>
<style lang="scss" scoped>
.weekly {
  background: #ffb309 url(@/assets/img/banners/money.png) no-repeat left 20px top 50%;
  box-shadow: 0px 2px 30px rgba(0, 0, 0, 0.2);
  border-radius: 30px;
  width: 100%;
  padding: 45px 60px 55px 185px;
  align-items: flex-end;
  justify-content: space-between;

  &__title {
    font-family: "Montserrat";
    font-weight: 700;
    font-size: 31px;
    line-height: 37px;
    color: #ffffff;
  }

  &__text {
    font-family: "Montserrat";
    font-weight: 500;
    font-size: 16px;
    line-height: 37px;
    color: #ffffff;
  }

  &__bonus {
    font-family: "Montserrat";
    font-weight: 700;
    font-size: 40px;
    line-height: 19px;
    color: #ffffff;
  }

  &__factor {
    padding: 13px;
    border: 1px solid #ffffff;
    filter: drop-shadow(0px 2px 30px rgba(0, 0, 0, 0.2));
    border-radius: 12px;
    align-items: center;
    justify-content: space-between;

    &-text {
      width: 160px;
      line-height: 19px;
    }
  }

  &__total {
    align-items: center;
    margin-left: 30px;

    &-text {
      min-width: auto;
      line-height: normal;
    }
  }

  &__button {
    font-size: 20px;
    padding: 0 30px;
  }
}


@media screen and (max-width:992px) {
  .weekly {
    padding: 25px 30px 25px 20px;
    background-position: top 30px right 50px;
    background-size: 10%;

    &__total {
      &-text {
        font-size: 30px;
      }

      img {
        width: 30px;
      }
    }
  }

}

@media screen and (max-width:768px) {
  .weekly {
    flex-direction: column;
    align-items: flex-start;

    &__main {
      margin-bottom: 15px;
    }

    &__text {
      font-size: 13px;
    }

  }
}

@media screen and (max-width:576px) {
  .weekly {
    &__title {
      font-size: 17px;
    }

    &__text {
      font-size: 11px;
      line-height: 150%;
    }

    &__bonus {
      font-size: 20px;
    }

    &__factor {
      padding: 9px;
      margin-top: 10px;
    }

    &__main {
      width: 100%;

      .wrapper {
        justify-content: space-between;
        align-items: flex-end;
      }
    }

    &__button {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
    }
  }
}

@media screen and (max-width:480px) {
  .weekly {
    background-position: top 20px right 15px;

    &__factor {
    }

    &__mult{
      flex-direction: column;
      align-items: center !important;
    }
    &__button{
      font-size: 12px;
    }
  }
}</style>
