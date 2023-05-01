<template>
  <div class="event wrapper" :style="{ background: color }">
    <img :src="img" alt="event" class="event__icon" />
    <div class="event__box">
      <h5 class="event__title">{{ title }}</h5>
      <p class="event__text">{{ text }}</p>
      <div class="wrapper event__bottom">
        <div class="wrapper event__bottom-wrapper">
          <p class="event__coins">{{ coins }}</p>
          <img src="@/assets/img/coin.png" alt="coin" class="event__coin" />
        </div>
        <AutorisationButton class="event__button"/>
      </div>
    </div>
  </div>
</template>
<script>
import AutorisationButton from '../UI/AutorisationButton.vue';

export default {
    props: ["title", "text", "img", "coins", "color"],
    components: { AutorisationButton }
};
</script>
<style lang="scss" scoped>
.event {
  box-shadow: 0px 2px 30px rgba(0, 0, 0, 0.2);
  border-radius: 30px;
  padding: 20px;
  &__box {
    display: flex;
    flex-direction: column;
  }
  &__title {
    font-family: "Montserrat";
    font-weight: 700;
    font-size: 24px;
    line-height: 37px;
    color: #ffffff;
  }
  &__text {
    font-family: "Montserrat";
    font-weight: 400;
    font-size: 20px;
    line-height: 25px;
    max-width: 250px;
    color: #ffffff;
  }
  &__bottom {
    margin-top: auto;
    justify-content: space-between;
    &-wrapper {
      align-items: center;
    }
  }
  &__coins {
    font-family: "Montserrat";
    font-weight: 700;
    font-size: 20px;
    line-height: 25px;
    color: #ffffff;
  }
  &__coin {
    width: 30px;
    margin-right: 25px;

  }
  &__button {
    font-size: 20px;
  }
  &__box{
    margin-left: 20px;
  }
}

@media screen and (max-width:768px) {
  .event{
    &__icon{
      height: 100px;
    }
    &__coin{
      height: auto;
    }
    &__title{
      font-size: 15px;
    }
    &__text{
      margin-bottom: 5px;
      font-size: 11px;
    }
    &__button{
      font-size: 13px;
    }
  }
}

@media screen and (max-width:480px) {
  .event{
    &__icon{
      display: none;
    }
    &__button{
      font-size: 12px;
    }
    &__text{
      line-height: 150%;
    }
  }
}
</style>
